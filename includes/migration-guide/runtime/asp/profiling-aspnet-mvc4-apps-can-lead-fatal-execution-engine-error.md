### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a><span data-ttu-id="248bd-101">分析 ASP.Net MVC4 应用可能导致严重的执行引擎错误</span><span class="sxs-lookup"><span data-stu-id="248bd-101">Profiling ASP.Net MVC4 apps can lead to Fatal Execution Engine Error</span></span>

|   |   |
|---|---|
|<span data-ttu-id="248bd-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="248bd-102">Details</span></span>|<span data-ttu-id="248bd-103">使用 NGEN /Profile 程序集的探查器可能会在启动时使已配置的 ASP.NET MVC4 应用程序出故障，引发“严重的执行引擎异常”</span><span class="sxs-lookup"><span data-stu-id="248bd-103">Profilers using NGEN /Profile assemblies may crash profiled ASP.NET MVC4 applications on startup with a 'Fatal Execution Engine Exception'</span></span>|
|<span data-ttu-id="248bd-104">建议</span><span class="sxs-lookup"><span data-stu-id="248bd-104">Suggestion</span></span>|<span data-ttu-id="248bd-105">此问题已在 .NET Framework 4.5.2 中解决。</span><span class="sxs-lookup"><span data-stu-id="248bd-105">This issue is fixed in the .NET Framework 4.5.2.</span></span> <span data-ttu-id="248bd-106">或者，探查器可通过在其事件掩码中指定 <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> 来避免此问题。</span><span class="sxs-lookup"><span data-stu-id="248bd-106">Alternatively, the profiler may avoid this issue by specifying <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> in its event mask.</span></span>|
|<span data-ttu-id="248bd-107">范围</span><span class="sxs-lookup"><span data-stu-id="248bd-107">Scope</span></span>|<span data-ttu-id="248bd-108">边缘</span><span class="sxs-lookup"><span data-stu-id="248bd-108">Edge</span></span>|
|<span data-ttu-id="248bd-109">版本</span><span class="sxs-lookup"><span data-stu-id="248bd-109">Version</span></span>|<span data-ttu-id="248bd-110">4.5</span><span class="sxs-lookup"><span data-stu-id="248bd-110">4.5</span></span>|
|<span data-ttu-id="248bd-111">类型</span><span class="sxs-lookup"><span data-stu-id="248bd-111">Type</span></span>|<span data-ttu-id="248bd-112">运行时</span><span class="sxs-lookup"><span data-stu-id="248bd-112">Runtime</span></span>|
