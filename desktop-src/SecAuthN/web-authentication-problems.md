---
description: In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungs Broker-APIs für Ihre Webseiten beschrieben.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Webauthentifizierungsprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571199"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="93717-103">Webauthentifizierungsprobleme</span><span class="sxs-lookup"><span data-stu-id="93717-103">Web authentication problems</span></span>

<span data-ttu-id="93717-104">In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungs Broker-APIs für Ihre Webseiten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="93717-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="93717-105">Betriebs Protokolle</span><span class="sxs-lookup"><span data-stu-id="93717-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="93717-106">Verwenden von "fddler" mit dem Webauthentifizierungs Broker</span><span class="sxs-lookup"><span data-stu-id="93717-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="93717-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93717-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="93717-108">Betriebsprotokolle</span><span class="sxs-lookup"><span data-stu-id="93717-108">Operational logs</span></span>

<span data-ttu-id="93717-109">Häufig können Sie anhand der Betriebsprotokolle ermitteln, was nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="93717-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="93717-110">Es gibt einen dedizierten Ereignisprotokoll Kanal Microsoft-Windows-webauth \\ Operational, mit dem Website Entwickler verstehen können, wie Ihre Webseiten vom Webauthentifizierungs Broker verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="93717-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="93717-111">Um dies zu aktivieren, starten Sie eventvwr.exe, und aktivieren Sie das Betriebsprotokoll unter den Anwendungs-und Dienstleistungen von \\ Microsoft \\ Windows \\ webauth.</span><span class="sxs-lookup"><span data-stu-id="93717-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="93717-112">Außerdem fügt der Webauthentifizierungs Broker eine eindeutige Zeichenfolge an die Benutzer-Agent-Zeichenfolge an, um sich selbst auf dem Webserver zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="93717-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="93717-113">Die Zeichenfolge lautet „MSAuthHost/1.0“.</span><span class="sxs-lookup"><span data-stu-id="93717-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="93717-114">Beachten Sie, dass sich die Versionsnummer ändern kann. Verlassen Sie sich also in Ihrem Code nicht auf diese Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="93717-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="93717-115">Ein Beispiel für die vollständige Benutzer-Agent-Zeichenfolge sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="93717-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="93717-116">Beispiel für die Verwendung von Betriebs Protokollen</span><span class="sxs-lookup"><span data-stu-id="93717-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="93717-117">Aktivieren von Betriebsprotokollen</span><span class="sxs-lookup"><span data-stu-id="93717-117">Enable operational logs</span></span>
2.  <span data-ttu-id="93717-118">Ausführen der Anwendung "" für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="93717-118">Run Contoso social application</span></span>![Ereignisanzeige mit webauth-Betriebsprotokollen](images/wab-figure15.png)
3.  <span data-ttu-id="93717-120">Die generierten Protokolleinträge können verwendet werden, um das Verhalten des Webauthentifizierungs Brokers ausführlicher nachzuvollziehen.</span><span class="sxs-lookup"><span data-stu-id="93717-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="93717-121">In diesem Fall können sie Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="93717-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="93717-122">Navigation – Starten: Protokolliert, wann AuthHost gestartet wird, und enthält Informationen zu den Start- und End-URLs.</span><span class="sxs-lookup"><span data-stu-id="93717-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![Veranschaulicht die Details von „Navigation – Starten“"](images/wab-figure16.png)
    -   <span data-ttu-id="93717-124">Navigation abgeschlossen: Protokolliert den Abschluss des Ladevorgangs einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="93717-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="93717-125">META-Tag: Protokolliert, wann ein META-Tag auftritt (einschließlich Details).</span><span class="sxs-lookup"><span data-stu-id="93717-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="93717-126">Navigation – Beenden: Die Navigation wurde vom Benutzer beendet.</span><span class="sxs-lookup"><span data-stu-id="93717-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="93717-127">Navigationsfehler: AuthHost ermittelt einen Navigationsfehler bei einer URL, einschließlich HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="93717-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="93717-128">Navigationsende: End-URL liegt vor.</span><span class="sxs-lookup"><span data-stu-id="93717-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="93717-129">Verwenden von "fddler" mit dem Webauthentifizierungs Broker</span><span class="sxs-lookup"><span data-stu-id="93717-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="93717-130">Der webdebugger von "fddler" kann mit Windows 8-Apps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93717-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="93717-131">Da AuthHost in einem eigenen App-Container ausgeführt wird, um Funktionen für private Netzwerke zu ermöglichen, müssen Sie einen Registrierungsschlüssel festlegen: Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="93717-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="93717-132">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **enableprivatenetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="93717-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="93717-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="93717-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="93717-134">Fügen Sie eine Regel für AuthHost hinzu, da darüber ausgehender Datenverkehr generiert wird.</span><span class="sxs-lookup"><span data-stu-id="93717-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
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

    

3.  <span data-ttu-id="93717-135">Fügen Sie Fiddler eine Firewallregel für eingehenden Datenverkehr hinzu.</span><span class="sxs-lookup"><span data-stu-id="93717-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="93717-136">Weitere Informationen finden Sie unter [Verwenden des webdebuggers für Windows Store-Apps mit dem webdebugger für Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span><span class="sxs-lookup"><span data-stu-id="93717-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="93717-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93717-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93717-138">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="93717-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="93717-139">Häufig gestellte Fragen zum Webauthentifizierungs Broker</span><span class="sxs-lookup"><span data-stu-id="93717-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="93717-140">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="93717-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="93717-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="93717-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
