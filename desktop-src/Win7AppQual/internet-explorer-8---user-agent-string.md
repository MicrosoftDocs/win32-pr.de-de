---
description: 'Internet Explorer 8: Benutzer-Agent-Zeichenfolge'
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: 'Internet Explorer 8: Benutzer-Agent-Zeichenfolge'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088238"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="f4e50-103">Internet Explorer 8: Benutzer-Agent-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f4e50-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f4e50-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="f4e50-104">Affected Platforms</span></span>

 <span data-ttu-id="f4e50-105">**Clients:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4e50-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="f4e50-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4e50-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="f4e50-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="f4e50-107">Feature Impact</span></span>

<span data-ttu-id="f4e50-108">**Schweregrad:** Mittel</span><span class="sxs-lookup"><span data-stu-id="f4e50-108">**Severity** - Medium</span></span>  
<span data-ttu-id="f4e50-109">**Häufigkeit** – Hoch</span><span class="sxs-lookup"><span data-stu-id="f4e50-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="f4e50-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4e50-110">Description</span></span>

<span data-ttu-id="f4e50-111">Die Benutzer-Agent-Zeichenfolge ist Internet Explorer Bezeichner, der Daten zu seiner Version und anderen Attributen für Webserver zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="f4e50-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="f4e50-112">Viele Webanwendungen basieren auf und piggyback auf der Zeichenfolge des IE-Benutzer-Agents.</span><span class="sxs-lookup"><span data-stu-id="f4e50-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="f4e50-113">Solche, die dies tun und von einer früheren Versionsnummer abhängen, sind davon abhängig.</span><span class="sxs-lookup"><span data-stu-id="f4e50-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="f4e50-114">Die Benutzer-Agent-Zeichenfolge enthält jetzt die Zeichenfolge "Trident/4.0", um die Unterscheidung zwischen der Internet Explorer 7-Benutzer-Agent-Zeichenfolge und der Internet Explorer 8-Benutzer-Agent-Zeichenfolge zu ermöglichen, wenn sie in Internet Explorer 7 Kompatibilitätsansicht.</span><span class="sxs-lookup"><span data-stu-id="f4e50-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="f4e50-115">Weitere Informationen finden Sie unter Grundlegendes zu Benutzer-Agent-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="f4e50-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f4e50-116">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="f4e50-116">Manifestation of Impact</span></span>

<span data-ttu-id="f4e50-117">Es gibt zwei bereiche, die sich auf diese Auswirken auswirken:</span><span class="sxs-lookup"><span data-stu-id="f4e50-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="f4e50-118">Webseiten, die die Benutzer-Agent-Zeichenfolge explizit überprüfen und die Internet Explorer 8-Benutzer-Agent-Zeichenfolge nicht unterstützen, werden möglicherweise nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4e50-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="f4e50-119">In den meisten Fällen bedeutet dies, dass die Seiten Benutzern den Inhalt blockieren, auf den sie zugreifen oder falsche oder falsch formatierte Inhalte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4e50-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="f4e50-120">Anwendungen, die Trident hosten (siehe Hosting und Wiederverwendung), verwenden standardmäßig Internet Explorer 7 mit der optionalen Webkomponente, haben jedoch keinen Zugriff auf Internet Explorer 8-Features.</span><span class="sxs-lookup"><span data-stu-id="f4e50-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="f4e50-121">Lösung</span><span class="sxs-lookup"><span data-stu-id="f4e50-121">Solution</span></span>

<span data-ttu-id="f4e50-122">Stellen Sie sicher, dass Ihre Anwendungen die neue MSIE 8.0-Version in der Benutzer-Agent-Zeichenfolge ordnungsgemäß verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f4e50-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="f4e50-123">Sie können auch die Internet Explorer 7-Kompatibilitätsansicht für diese Anwendungen basierend auf Internet Explorer 7 wählen.</span><span class="sxs-lookup"><span data-stu-id="f4e50-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="f4e50-124">Dies kann mit Metatags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f4e50-124">This can be done with meta tags.</span></span> <span data-ttu-id="f4e50-125">Weitere Informationen finden Sie in der Erläuterung unter Grundlegendes zu Benutzer-Agent-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="f4e50-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="f4e50-126">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests</span><span class="sxs-lookup"><span data-stu-id="f4e50-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="f4e50-127">Führen Sie Ihre Anwendungen und Webseiten in einer Internet Explorer 8-Umgebung unter Windows Vista oder Windows XP aus, um sicherzustellen, dass sie sich auf die gewünschte Weise verhalten.</span><span class="sxs-lookup"><span data-stu-id="f4e50-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="f4e50-128">Alternativ können Sie das mit dem Application Compatibility Toolkit (ACT) bereitgestellte Internet Explorer Compatibility Test Tool (IECTT) ausführen, um mögliche Probleme aufgrund von Sicherheitsupdates zu finden.</span><span class="sxs-lookup"><span data-stu-id="f4e50-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f4e50-129">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4e50-129">Links to Other Resources</span></span>

-   <span data-ttu-id="f4e50-130">[Grundlegendes zu Benutzer-Agent-Zeichenfolgen](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4e50-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="f4e50-131">Internet Explorer 8 User-Agent Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f4e50-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="f4e50-132">Benutzer-Agent-Zeichenfolge und Versionsvektor</span><span class="sxs-lookup"><span data-stu-id="f4e50-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="f4e50-133">[Hosting und Wiederverwendung](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4e50-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="f4e50-134">Herunterladen des Anwendungskompatibilitätstoolkits</span><span class="sxs-lookup"><span data-stu-id="f4e50-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="f4e50-135">[Bekannte probleme mit Internet Explorer-Sicherheitsfeatures](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="f4e50-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
