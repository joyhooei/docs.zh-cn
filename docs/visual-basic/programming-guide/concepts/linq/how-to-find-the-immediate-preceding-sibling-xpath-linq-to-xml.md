---
title: 如何： 查找紧前面的同级 (XPATH-LINQ to XML) (Visual Basic)
ms.date: 07/20/2015
ms.assetid: ec046283-9fe2-4440-b295-860bf700099d
ms.openlocfilehash: 47ba557343d0f691c2ee0f2c56102df313ecfb30
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33641103"
---
# <a name="how-to-find-the-immediate-preceding-sibling-xpath-linq-to-xml-visual-basic"></a>如何： 查找紧前面的同级 (XPATH-LINQ to XML) (Visual Basic)
有时，您需要查找某一节点的前面紧邻同级。 由于与 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 相比，XPath 中前面紧邻轴的位置谓词的语义同，因此这是一个更值得关注的比较。  
  
## <a name="example"></a>示例  
 在本示例中，[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 查询使用 <xref:System.Linq.Enumerable.Last%2A> 运算符查找由 <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A> 返回的集合中的最后一个节点。 相比之下，XPath 表达式使用值为 1 的谓词来查找前面紧邻的元素。  
  
```vb  
Dim root As XElement = _   
    <Root>  
        <Child1/>  
        <Child2/>  
        <Child3/>  
        <Child4/>  
    </Root>  
Dim child4 As XElement = root.Element("Child4")  
  
' LINQ to XML query  
Dim el1 As XElement = child4.ElementsBeforeSelf().Last()  
  
' XPath expression  
Dim el2 As XElement = _  
    DirectCast(child4.XPathEvaluate("preceding-sibling::*[1]"),  _  
    IEnumerable).Cast(Of XElement)().First()  
  
If el1 Is el2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(el1)  
```  
  
 该示例产生下面的输出：  
  
```  
Results are identical  
<Child3 />  
```  
  
## <a name="see-also"></a>请参阅  
 [LINQ to XML 针对 XPath 用户 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
