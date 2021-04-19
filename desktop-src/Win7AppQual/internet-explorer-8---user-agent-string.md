---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-Benutzer-Agent-Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea44572f32e252a4e1d4dc2209e411834c12d4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314793"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="416b4-103">Internet Explorer 8-Benutzer-Agent-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="416b4-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="416b4-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="416b4-104">Affected Platforms</span></span>

 <span data-ttu-id="416b4-105">**Clients** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="416b4-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="416b4-106">**Server** -Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="416b4-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="416b4-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="416b4-107">Feature Impact</span></span>

<span data-ttu-id="416b4-108">**Schweregrad** -Mittel</span><span class="sxs-lookup"><span data-stu-id="416b4-108">**Severity** - Medium</span></span>  
<span data-ttu-id="416b4-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="416b4-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="416b4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="416b4-110">Description</span></span>

<span data-ttu-id="416b4-111">Die Benutzer-Agent-Zeichenfolge ist der Internet Explorer-Bezeichner, der Daten über seine Version und andere Attribute für Webserver bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="416b4-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="416b4-112">Viele Webanwendungen verlassen sich auf die Benutzer-Agent-Zeichenfolge des IE-Benutzers und greifen darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="416b4-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="416b4-113">Solche, die dies tun und von einer früheren Versionsnummer abhängen, sind betroffen.</span><span class="sxs-lookup"><span data-stu-id="416b4-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="416b4-114">Die Zeichenfolge des Benutzer-Agents enthält nun die Zeichenfolge "dreident/4.0", um Unterschiede zwischen der Benutzer-Agent-Zeichenfolge von Internet Explorer 7 und der Zeichenfolge des Benutzer-Agents von Internet Explorer 8 bei Ausführung in der Kompatibilitäts Ansicht von Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="416b4-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="416b4-115">Weitere Informationen finden Sie Untergrund Legendes zu Benutzer-Agent</span><span class="sxs-lookup"><span data-stu-id="416b4-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="416b4-116">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="416b4-116">Manifestation of Impact</span></span>

<span data-ttu-id="416b4-117">Es gibt zwei betroffene Bereiche:</span><span class="sxs-lookup"><span data-stu-id="416b4-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="416b4-118">Webseiten, die die Benutzer-Agent-Zeichenfolge explizit überprüfen und die Benutzer-Agent-Zeichenfolge von Internet Explorer 8 nicht unterstützen, werden möglicherweise nicht</span><span class="sxs-lookup"><span data-stu-id="416b4-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="416b4-119">In den meisten Fällen bedeutet dies, dass die Seiten Benutzer aus dem Inhalt blockieren, auf den Sie zugreifen möchten, oder dass falsche oder falsch formatierte Inhalte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="416b4-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="416b4-120">Anwendungen, die einen Einzug hosten (siehe Hosting und Wiederverwendung), werden standardmäßig Internet Explorer 7 verwendet, wobei die optionale Webkomponente verwendet wird. Sie haben jedoch keinen Zugriff auf Internet Explorer 8-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="416b4-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="416b4-121">Lösung</span><span class="sxs-lookup"><span data-stu-id="416b4-121">Solution</span></span>

<span data-ttu-id="416b4-122">Stellen Sie sicher, dass die Anwendung die neue Version "MSIE 8,0" in der Zeichenfolge des Benutzer-Agents ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="416b4-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="416b4-123">Sie können auch die Kompatibilitäts Ansicht von Internet Explorer 7 für Anwendungen, die auf Internet Explorer 7 basieren, anmelden.</span><span class="sxs-lookup"><span data-stu-id="416b4-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="416b4-124">Dies kann mit Meta-Tags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="416b4-124">This can be done with meta tags.</span></span> <span data-ttu-id="416b4-125">Weitere Informationen finden Sie Untergrund Legendes zu Benutzer-Agent-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="416b4-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="416b4-126">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="416b4-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="416b4-127">Führen Sie Ihre Anwendungen und Webseiten in einer Internet Explorer 8-Umgebung unter Windows Vista oder Windows XP aus, um sicherzustellen, dass Sie sich auf die gewünschte Weise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="416b4-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="416b4-128">Alternativ können Sie das mit dem Anwendungskompatibilitäts-Toolkit (Application Compatibility Toolkit, Act) bereitgestellte Internet Explorer Compatibility Test Tool (iectt) ausführen, um mögliche Probleme aufgrund von Updates der Sicherheitsfeatures zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="416b4-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="416b4-129">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="416b4-129">Links to Other Resources</span></span>

-   <span data-ttu-id="416b4-130">[Grundlegendes zu Benutzer-Agent](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="416b4-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="416b4-131">Internet Explorer 8-User-Agent Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="416b4-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="416b4-132">Benutzer-Agent-Zeichenfolge und Versions Vektor</span><span class="sxs-lookup"><span data-stu-id="416b4-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="416b4-133">[Hosting und Wiederverwendung](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="416b4-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="416b4-134">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="416b4-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="416b4-135">[Bekannte Probleme mit der Internet Explorer-Sicherheitsfunktion](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="416b4-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
