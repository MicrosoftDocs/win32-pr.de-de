---
title: URIs in Windows 8.1
description: Windows 8.1 nur HTTPS-URIs und keine http-URIs zulässt.
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390857"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="1b6eb-103">Windows 8.1 nur HTTPS-URIs und keine http-URIs zulässt.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="1b6eb-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="1b6eb-104">Platforms</span></span>

<dl> <span data-ttu-id="1b6eb-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1b6eb-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="1b6eb-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1b6eb-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="1b6eb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b6eb-107">Description</span></span>

<span data-ttu-id="1b6eb-108">Apps, die für Windows 8 erstellt wurden, können http-und HTTPS-URIs in Ihre Anwendungsinhalts-URIs einschließen. für Windows 8.1 erstellten apps dürfen jedoch nur HTTPS-URIs enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="1b6eb-109">Die einzige Ausnahme ist für dynamische contenturirules, die in der AppxManifest.xml Datei der APP angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="1b6eb-110">Mit dynamischen contenturirules-Regeln können apps auf zusätzliche Domänen oder Netzwerkressourcen zugreifen, die vom Administrator bereitgestellt werden, z. b. Gruppenrichtlinie URIs.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="1b6eb-111">Dynamische contenturirules sind jedoch nur für Windows Store-Apps verfügbar, wenn Sie die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="1b6eb-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="1b6eb-112">Der Gruppenrichtlinie ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="1b6eb-113">Das Paket hat die enterprisauthentication-Funktion angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="1b6eb-114">Osmaxversiongetesteten des Pakets ist Windows 8.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="1b6eb-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="1b6eb-115">Die neuen Einschränkungen in Windows 8.1 sind Teil der verbesserten Sicherheitseinschränkungen, um die Plattform weiter zu schützen.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="1b6eb-116">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="1b6eb-116">Manifestations</span></span>

<span data-ttu-id="1b6eb-117">Beim Ausführen einer APP, die für Windows 8 auf Windows 8.1 erstellt wurde, ist die Verwendung von http-URIs in den [applicationcontenturirules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) zulässig.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="1b6eb-118">Gegenmaßnahmen</span><span class="sxs-lookup"><span data-stu-id="1b6eb-118">Mitigations</span></span>

<span data-ttu-id="1b6eb-119">Es wird empfohlen, dass WWA-Entwickler von [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) zum [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) -Steuerelement wechseln (<x-ms-WebView>).</span><span class="sxs-lookup"><span data-stu-id="1b6eb-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="1b6eb-120">Wenn Sie jedoch Unterstützung für AppCache, indexeddb, Geolokation oder programmatischen Zugriff auf die Zwischenablage benötigen, müssen Sie weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="1b6eb-121">für Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-121">for Windows 8.1.</span></span>

<span data-ttu-id="1b6eb-122">Fortgesetzte Verwendung von</span><span class="sxs-lookup"><span data-stu-id="1b6eb-122">Continued usage of</span></span> <iframe> <span data-ttu-id="1b6eb-123">für Remote Inhalte ist in den applicationcontenturirules-Funktionen für die APP ein neuer Eintrag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="1b6eb-124">Apps mit WebView erfordern neue Einträge in applicationcontenturirules, wenn der Webinhalt Window. extern. Notify zum Erstellen eines [scriptnotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) -Ereignisses aufrufen muss.</span><span class="sxs-lookup"><span data-stu-id="1b6eb-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="1b6eb-125">Wenn Sie nicht über Visual Studio verfügen, können Sie das App-Manifest aktualisieren, indem Sie den folgenden XML-Code hinzufügen, einschließlich der Platzhalter für Unterdomänen (z. b. https:// \* . Microsoft.com):</span><span class="sxs-lookup"><span data-stu-id="1b6eb-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a><span data-ttu-id="1b6eb-126">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1b6eb-126">Resources</span></span>

-   [<span data-ttu-id="1b6eb-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="1b6eb-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="1b6eb-128"><iframe> Element- \| <iframe> Objekt</span><span class="sxs-lookup"><span data-stu-id="1b6eb-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="1b6eb-129">WebView-Klasse</span><span class="sxs-lookup"><span data-stu-id="1b6eb-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="1b6eb-130">WebView. scriptnotify-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1b6eb-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 