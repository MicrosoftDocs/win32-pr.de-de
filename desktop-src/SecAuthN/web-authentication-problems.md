---
description: In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungsbroker-APIs für Ihre Webseiten beschrieben.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Webauthentifizierungsprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f996527c58b9620b8417ac3e6cdd6e0f61bd5217
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353663"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="2a8f1-103">Webauthentifizierungsprobleme</span><span class="sxs-lookup"><span data-stu-id="2a8f1-103">Web authentication problems</span></span>

<span data-ttu-id="2a8f1-104">In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungsbroker-APIs für Ihre Webseiten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="2a8f1-105">Betriebsprotokolle</span><span class="sxs-lookup"><span data-stu-id="2a8f1-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="2a8f1-106">Verwenden von Fiddler mit dem Webauthentifizierungsbroker</span><span class="sxs-lookup"><span data-stu-id="2a8f1-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="2a8f1-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2a8f1-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="2a8f1-108">Betriebsprotokolle</span><span class="sxs-lookup"><span data-stu-id="2a8f1-108">Operational logs</span></span>

<span data-ttu-id="2a8f1-109">Häufig können Sie anhand der Betriebsprotokolle ermitteln, was nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="2a8f1-110">Es gibt einen dedizierten Ereignisprotokollkanal Microsoft-Windows-WebAuth Operational, mit dem Websiteentwickler verstehen können, wie ihre Webseiten vom \\ Webauthentifizierungsbroker verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="2a8f1-111">Um sie zu aktivieren, starten Sie eventvwr.exe, und aktivieren Sie das Betriebsprotokoll unter Anwendung und Dienste \\ Microsoft \\ Windows \\ WebAuth.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="2a8f1-112">Außerdem fügt der Webauthentifizierungsbroker eine eindeutige Zeichenfolge an die Benutzer-Agent-Zeichenfolge an, um sich auf dem Webserver zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="2a8f1-113">Die Zeichenfolge lautet „MSAuthHost/1.0“.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="2a8f1-114">Beachten Sie, dass sich die Versionsnummer ändern kann. Verlassen Sie sich also in Ihrem Code nicht auf diese Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="2a8f1-115">Ein Beispiel für die vollständige Benutzer-Agent-Zeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2a8f1-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="2a8f1-116">Beispiel für die Verwendung von Betriebsprotokollen</span><span class="sxs-lookup"><span data-stu-id="2a8f1-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="2a8f1-117">Aktivieren von Betriebsprotokollen</span><span class="sxs-lookup"><span data-stu-id="2a8f1-117">Enable operational logs</span></span>
2.  <span data-ttu-id="2a8f1-118">Ausführen einer Contoso-Anwendung für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="2a8f1-118">Run Contoso social application</span></span>![Ereignisanzeige mit webauth-Betriebsprotokollen](images/wab-figure15.png)
3.  <span data-ttu-id="2a8f1-120">Die generierten Protokolleinträge können verwendet werden, um das Verhalten des Webauthentifizierungsbrokers ausführlicher zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="2a8f1-121">In diesem Fall können sie Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="2a8f1-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="2a8f1-122">Navigation – Starten: Protokolliert, wann AuthHost gestartet wird, und enthält Informationen zu den Start- und End-URLs.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![Veranschaulicht die Details von „Navigation – Starten“"](images/wab-figure16.png)
    -   <span data-ttu-id="2a8f1-124">Navigation abgeschlossen: Protokolliert den Abschluss des Ladevorgangs einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="2a8f1-125">META-Tag: Protokolliert, wann ein META-Tag auftritt (einschließlich Details).</span><span class="sxs-lookup"><span data-stu-id="2a8f1-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="2a8f1-126">Navigation – Beenden: Die Navigation wurde vom Benutzer beendet.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="2a8f1-127">Navigationsfehler: AuthHost ermittelt einen Navigationsfehler bei einer URL, einschließlich HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="2a8f1-128">Navigationsende: End-URL liegt vor.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="2a8f1-129">Verwenden von Fiddler mit dem Webauthentifizierungsbroker</span><span class="sxs-lookup"><span data-stu-id="2a8f1-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="2a8f1-130">Der Fiddler-Webdebugger kann mit Windows 8 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="2a8f1-131">Da AuthHost in einem eigenen App-Container ausgeführt wird, um Funktionen für private Netzwerke zu ermöglichen, müssen Sie einen Registrierungsschlüssel festlegen: Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="2a8f1-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="2a8f1-132">**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Image File Execution \\ **Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="2a8f1-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="2a8f1-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="2a8f1-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="2a8f1-134">Fügen Sie eine Regel für AuthHost hinzu, da darüber ausgehender Datenverkehr generiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  <span data-ttu-id="2a8f1-135">Fügen Sie Fiddler eine Firewallregel für eingehenden Datenverkehr hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a8f1-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="2a8f1-136">Weitere Informationen finden Sie im [Blog zur Verwendung des Fiddler-Webdebuggers mit Windows Store Apps.](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications)</span><span class="sxs-lookup"><span data-stu-id="2a8f1-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a8f1-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a8f1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a8f1-138">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="2a8f1-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="2a8f1-139">Häufig gestellte Fragen zum Webauthentifizierungsbroker</span><span class="sxs-lookup"><span data-stu-id="2a8f1-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)
</dt> <dt>

[<span data-ttu-id="2a8f1-140">Beispiel-App für das Webauthentifizierungsbroker-SDK</span><span class="sxs-lookup"><span data-stu-id="2a8f1-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="2a8f1-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="2a8f1-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
