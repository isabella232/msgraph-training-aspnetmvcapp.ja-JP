<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="6dc2b-101">Visual Studio を開き、[**ファイル > 新しい > プロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-101">Open Visual Studio, and select **File > New > Project**.</span></span> <span data-ttu-id="6dc2b-102">[**新しいプロジェクト**] ダイアログボックスで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-102">In the **New Project** dialog, do the following:</span></span>

1. <span data-ttu-id="6dc2b-103">**Visual C# > Web > テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-103">Select **Templates > Visual C# > Web**.</span></span>
1. <span data-ttu-id="6dc2b-104">[ **ASP.NET Web アプリケーション (.Net Framework)**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-104">Select **ASP.NET Web Application (.NET Framework)**.</span></span>
1. <span data-ttu-id="6dc2b-105">プロジェクトの名前については、「グラフを入力してください」**というチュートリアル**を行います。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-105">Enter **graph-tutorial** for the Name of the project.</span></span>

    ![Visual Studio 2017 [新しいプロジェクトの作成] ダイアログ](./images/vs-new-project-01.png)

    > [!NOTE]
    > <span data-ttu-id="6dc2b-107">これらのラボ手順で指定した Visual Studio プロジェクトに対して、まったく同じ名前を入力してください。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-107">Ensure that you enter the exact same name for the Visual Studio Project that is specified in these lab instructions.</span></span> <span data-ttu-id="6dc2b-108">Visual Studio プロジェクト名は、コード内の名前空間の一部になります。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-108">The Visual Studio Project name becomes part of the namespace in the code.</span></span> <span data-ttu-id="6dc2b-109">これらの手順内のコードは、この手順で指定した Visual Studio プロジェクト名に一致する名前空間によって決まります。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-109">The code inside these instructions depends on the namespace matching the Visual Studio Project name specified in these instructions.</span></span> <span data-ttu-id="6dc2b-110">別のプロジェクト名を使用すると、プロジェクトの作成時に入力した Visual Studio プロジェクト名と一致するようにすべての名前空間を調整しない限り、コードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-110">If you use a different project name the code will not compile unless you adjust all the namespaces to match the Visual Studio Project name you enter when you create the project.</span></span>

1. <span data-ttu-id="6dc2b-111">**[OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-111">Select **OK**.</span></span> <span data-ttu-id="6dc2b-112">[ **ASP.NET Web アプリケーションプロジェクトの新規作成**] ダイアログボックスで、[ **MVC** ( **ASP.NET 4.7.2 Templates**)] を選択し、[ **OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-112">In the **New ASP.NET Web Application Project** dialog, select **MVC** (under **ASP.NET 4.7.2 Templates**) and select **OK**.</span></span>

1. <span data-ttu-id="6dc2b-113">**F5**キーを押すか、デバッグ > 選択して**デバッグを開始**します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-113">Press **F5** or select **Debug > Start Debugging**.</span></span> <span data-ttu-id="6dc2b-114">すべてが動作している場合は、既定のブラウザーが開き、既定の ASP.NET ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-114">If everything is working, your default browser should open and display a default ASP.NET page.</span></span>

## <a name="add-nuget-packages"></a><span data-ttu-id="6dc2b-115">NuGet パッケージを追加する</span><span class="sxs-lookup"><span data-stu-id="6dc2b-115">Add NuGet packages</span></span>

<span data-ttu-id="6dc2b-116">に進む前に、 `bootstrap` nuget パッケージを更新し、後で使用する追加の nuget パッケージをいくつかインストールします。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-116">Before moving on, update the `bootstrap` NuGet package, and install some additional NuGet packages that you will use later.</span></span>

- <span data-ttu-id="6dc2b-117">[Owin web](https://www.nuget.org/packages/Microsoft.Owin.Host.SystemWeb/)を使用して、ASP.NET アプリケーションで[Owin](http://owin.org/)インターフェイスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-117">[Microsoft.Owin.Host.SystemWeb](https://www.nuget.org/packages/Microsoft.Owin.Host.SystemWeb/) to enable the [OWIN](http://owin.org/) interfaces in the ASP.NET application.</span></span>
- <span data-ttu-id="6dc2b-118">Owin Azure で OpenID Connect 認証を実行するための[OpenIdConnect](https://www.nuget.org/packages/Microsoft.Owin.Security.OpenIdConnect/) 。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-118">[Microsoft.Owin.Security.OpenIdConnect](https://www.nuget.org/packages/Microsoft.Owin.Security.OpenIdConnect/) for doing OpenID Connect authentication with Azure.</span></span>
- <span data-ttu-id="6dc2b-119">Cookie ベースの認証を有効にする[Owin](https://www.nuget.org/packages/Microsoft.Owin.Security.Cookies/) 。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-119">[Microsoft.Owin.Security.Cookies](https://www.nuget.org/packages/Microsoft.Owin.Security.Cookies/) to enable cookie-based authentication.</span></span>
- <span data-ttu-id="6dc2b-120">アクセストークンを要求および管理するための[id](https://www.nuget.org/packages/Microsoft.Identity.Client/) 。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-120">[Microsoft.Identity.Client](https://www.nuget.org/packages/Microsoft.Identity.Client/) for requesting and managing access tokens.</span></span>
- <span data-ttu-id="6dc2b-121">Microsoft Graph に電話をかけるための[グラフ](https://www.nuget.org/packages/Microsoft.Graph/)です。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-121">[Microsoft.Graph](https://www.nuget.org/packages/Microsoft.Graph/) for making calls to Microsoft Graph.</span></span>

1. <span data-ttu-id="6dc2b-122">[**ツール > NuGet パッケージマネージャー > パッケージマネージャーコンソール**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-122">Select **Tools > NuGet Package Manager > Package Manager Console**.</span></span>
1. <span data-ttu-id="6dc2b-123">パッケージマネージャーコンソールで、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-123">In the Package Manager Console, enter the following commands.</span></span>

    ```Powershell
    Update-Package bootstrap
    Install-Package Microsoft.Owin.Host.SystemWeb
    Install-Package Microsoft.Owin.Security.OpenIdConnect
    Install-Package Microsoft.Owin.Security.Cookies
    Install-Package Microsoft.Identity.Client -Version 3.0.8
    Install-Package Microsoft.Graph -Version 1.15.0
    ```

## <a name="design-the-app"></a><span data-ttu-id="6dc2b-124">アプリを設計する</span><span class="sxs-lookup"><span data-stu-id="6dc2b-124">Design the app</span></span>

<span data-ttu-id="6dc2b-125">このセクションでは、アプリケーションの基本的な構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-125">In this section you will create the basic structure of the application.</span></span>

1. <span data-ttu-id="6dc2b-126">基本的な OWIN startup クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-126">Create a basic OWIN startup class.</span></span> <span data-ttu-id="6dc2b-127">ソリューションエクスプローラーで`graph-tutorial`フォルダーを右クリックして、[**新しいアイテムの追加 >**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-127">Right-click the `graph-tutorial` folder in Solution Explorer and select **Add > New Item**.</span></span> <span data-ttu-id="6dc2b-128">**OWIN Startup クラス**テンプレートを選択し、ファイル`Startup.cs`の名前を指定して、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-128">Choose the **OWIN Startup Class** template, name the file `Startup.cs`, and select **Add**.</span></span>

1. <span data-ttu-id="6dc2b-129">ソリューションエクスプローラーで [**モデル**] フォルダーを右クリックし、[ **> クラスの追加**] を選択します。クラス`Alert`の名前を指定して、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-129">Right-click the **Models** folder in Solution Explorer and select **Add > Class...**. Name the class `Alert` and select **Add**.</span></span> <span data-ttu-id="6dc2b-130">に`Alert.cs`次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-130">Add the following code in `Alert.cs`.</span></span> <span data-ttu-id="6dc2b-131">このクラスを使用して、アプリのビューでエラーメッセージをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-131">You'll use this class to flash error messages in the app's views.</span></span>

    ```cs
    namespace graph_tutorial.Models
    {
        public class Alert
        {
            public const string AlertKey = "TempDataAlerts";
            public string Message { get; set; }
            public string Debug { get; set; }
        }
    }
    ```

1. <span data-ttu-id="6dc2b-132">`./Views/Shared/_Layout.cshtml`ファイルを開き、その内容全体を次のコードに置き換えて、アプリのグローバルレイアウトを更新します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-132">Open the `./Views/Shared/_Layout.cshtml` file, and replace its entire contents with the following code to update the global layout of the app.</span></span>

    ```html
    @{
        var alerts = TempData.ContainsKey(graph_tutorial.Models.Alert.AlertKey) ?
            (List<graph_tutorial.Models.Alert>)TempData[graph_tutorial.Models.Alert.AlertKey] :
            new List<graph_tutorial.Models.Alert>();
    }

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>ASP.NET Graph Tutorial</title>
        @Styles.Render("~/Content/css")
        @Scripts.Render("~/bundles/modernizr")

        <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.0/css/all.css"
              integrity="sha384-lKuwvrZot6UHsBSfcMvOkWwlCMgc0TaWr+30HWe3a4ltaBwTZhyTEggF5tJv8tbt"
              crossorigin="anonymous">
    </head>

    <body>
        <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
            <div class="container">
                @Html.ActionLink("ASP.NET Graph Tutorial", "Index", "Home", new { area = "" }, new { @class = "navbar-brand" })
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarCollapse"
                        aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarCollapse">
                    <ul class="navbar-nav mr-auto">
                        <li class="nav-item">
                            @Html.ActionLink("Home", "Index", "Home", new { area = "" },
                                new { @class = ViewBag.Current == "Home" ? "nav-link active" : "nav-link" })
                        </li>
                        @if (Request.IsAuthenticated)
                        {
                            <li class="nav-item" data-turbolinks="false">
                                @Html.ActionLink("Calendar", "Index", "Calendar", new { area = "" },
                                    new { @class = ViewBag.Current == "Calendar" ? "nav-link active" : "nav-link" })
                            </li>
                        }
                    </ul>
                    <ul class="navbar-nav justify-content-end">
                        <li class="nav-item">
                            <a class="nav-link" href="https://developer.microsoft.com/graph/docs/concepts/overview" target="_blank">
                                <i class="fas fa-external-link-alt mr-1"></i>Docs
                            </a>
                        </li>
                        @if (Request.IsAuthenticated)
                        {
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">
                                    @if (!string.IsNullOrEmpty(ViewBag.User.Avatar))
                                    {
                                        <img src="@ViewBag.User.Avatar" class="rounded-circle align-self-center mr-2" style="width: 32px;">
                                    }
                                    else
                                    {
                                        <i class="far fa-user-circle fa-lg rounded-circle align-self-center mr-2" style="width: 32px;"></i>
                                    }
                                </a>
                                <div class="dropdown-menu dropdown-menu-right">
                                    <h5 class="dropdown-item-text mb-0">@ViewBag.User.DisplayName</h5>
                                    <p class="dropdown-item-text text-muted mb-0">@ViewBag.User.Email</p>
                                    <div class="dropdown-divider"></div>
                                    @Html.ActionLink("Sign Out", "SignOut", "Account", new { area = "" }, new { @class = "dropdown-item" })
                                </div>
                            </li>
                        }
                        else
                        {
                            <li class="nav-item">
                                @Html.ActionLink("Sign In", "SignIn", "Account", new { area = "" }, new { @class = "nav-link" })
                            </li>
                        }
                    </ul>
                </div>
            </div>
        </nav>
        <main role="main" class="container">
            @foreach (var alert in alerts)
            {
                <div class="alert alert-danger" role="alert">
                    <p class="mb-3">@alert.Message</p>
                    @if (!string.IsNullOrEmpty(alert.Debug))
                    {
                        <pre class="alert-pre border bg-light p-2"><code>@alert.Debug</code></pre>
                    }
                </div>
            }

            @RenderBody()
        </main>
        @Scripts.Render("~/bundles/jquery")
        @Scripts.Render("~/bundles/bootstrap")
        @RenderSection("scripts", required: false)
    </body>
    </html>
    ```

    <span data-ttu-id="6dc2b-133">このコードでは、単純なスタイル設定[](https://fontawesome.com/)のために[ブートストラップ](https://getbootstrap.com/)が追加されています。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-133">This code adds [Bootstrap](https://getbootstrap.com/) for simple styling, and [Font Awesome](https://fontawesome.com/) for some simple icons.</span></span> <span data-ttu-id="6dc2b-134">また、ナビゲーションバーのあるグローバルレイアウトを定義し、その`Alert`クラスを使用して通知を表示します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-134">It also defines a global layout with a nav bar, and uses the `Alert` class to display any alerts.</span></span>

1. <span data-ttu-id="6dc2b-135">を`Content/Site.css`開いて、コンテンツ全体を次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-135">Open `Content/Site.css` and replace its entire contents with the following code.</span></span>

    ```css
    body {
      padding-top: 4.5rem;
    }

    .alert-pre {
      word-wrap: break-word;
      word-break: break-all;
      white-space: pre-wrap;
    }
    ```

1. <span data-ttu-id="6dc2b-136">`Views/Home/index.cshtml`ファイルを開き、その内容を次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-136">Open the `Views/Home/index.cshtml` file and replace its contents with the following.</span></span>

    ```html
    @{
        ViewBag.Current = "Home";
    }

    <div class="jumbotron">
        <h1>ASP.NET Graph Tutorial</h1>
        <p class="lead">This sample app shows how to use the Microsoft Graph API to access Outlook and OneDrive data from ASP.NET</p>
        @if (Request.IsAuthenticated)
        {
            <h4>Welcome @ViewBag.User.DisplayName!</h4>
            <p>Use the navigation bar at the top of the page to get started.</p>
        }
        else
        {
            @Html.ActionLink("Click here to sign in", "SignIn", "Account", new { area = "" }, new { @class = "btn btn-primary btn-large" })
        }
    </div>
    ```

1. <span data-ttu-id="6dc2b-137">ソリューションエクスプローラーで [**コントローラー** ] フォルダーを右クリックし、[ **> コントローラーの追加**] を選択します。[ **MVC 5 コントローラー-空**] を選択し、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-137">Right-click the **Controllers** folder in Solution Explorer and select **Add > Controller...**. Choose **MVC 5 Controller - Empty** and select **Add**.</span></span> <span data-ttu-id="6dc2b-138">コントローラー `BaseController`の名前を指定して、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-138">Name the controller `BaseController` and select **Add**.</span></span> <span data-ttu-id="6dc2b-139">の内容を以下のコードと置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-139">Replace the contents of `BaseController.cs` with the following code.</span></span>

    ```cs
    using graph_tutorial.Models;
    using System.Collections.Generic;
    using System.Web.Mvc;

    namespace graph_tutorial.Controllers
    {
        public abstract class BaseController : Controller
        {
            protected void Flash(string message, string debug=null)
            {
                var alerts = TempData.ContainsKey(Alert.AlertKey) ?
                    (List<Alert>)TempData[Alert.AlertKey] :
                    new List<Alert>();

                alerts.Add(new Alert
                {
                    Message = message,
                    Debug = debug
                });

                TempData[Alert.AlertKey] = alerts;
            }
        }
    }
    ```

    <span data-ttu-id="6dc2b-140">すべてのコントローラーは、この基本コントローラクラスから継承して、 `Flash`関数へのアクセスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-140">Any controller can inherit from this base controller class to gain access to the `Flash` function.</span></span> <span data-ttu-id="6dc2b-141">継承元`HomeController` `BaseController`のクラスを更新します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-141">Update the `HomeController` class to inherit from `BaseController`.</span></span>

1. <span data-ttu-id="6dc2b-142">を`Controllers/HomeController.cs`開き、 `public class HomeController : Controller`行を次のように変更します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-142">Open `Controllers/HomeController.cs` and change the `public class HomeController : Controller` line to:</span></span>

    ```cs
    public class HomeController : BaseController
    ```

1. <span data-ttu-id="6dc2b-143">すべての変更を保存し、サーバーを再起動します。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-143">Save all of your changes and restart the server.</span></span> <span data-ttu-id="6dc2b-144">この時点で、アプリの外観は大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="6dc2b-144">Now, the app should look very different.</span></span>

    ![再設計されたホームページのスクリーンショット](./images/create-app-01.png)
