---
description: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116068"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="c17d8-103">Benutzeroberfläche: Hohe DPI-Werte</span><span class="sxs-lookup"><span data-stu-id="c17d8-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c17d8-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="c17d8-104">Affected Platforms</span></span>

 <span data-ttu-id="c17d8-105">**Clients** : Windows XP \| Windows Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="c17d8-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="c17d8-106">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="c17d8-106">Feature Impact</span></span>

<span data-ttu-id="c17d8-107">**Schweregrad –** Mittel</span><span class="sxs-lookup"><span data-stu-id="c17d8-107">**Severity** - Medium</span></span>  
<span data-ttu-id="c17d8-108">**Häufigkeit** – Mittel</span><span class="sxs-lookup"><span data-stu-id="c17d8-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="c17d8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c17d8-109">Description</span></span>

<span data-ttu-id="c17d8-110">Das Ziel besteht darin, Endbenutzer zu ermutigen, ihre Anzeigen auf eine native Auflösung festzulegen und DPI anstelle der Bildschirmauflösung zu verwenden, um die Größe des angezeigten Texts und der Bilder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c17d8-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="c17d8-111">Windows 7 kann einen Standard-DPI auf Neuinstallationen auf Computern automatisch erkennen und konfigurieren, die von ihren OEMs mithilfe von DPI-Einstellungen konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c17d8-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="c17d8-112">Es gibt Tools, mit denen Sie Anwendungen entwerfen können, die hohe DPI-Werte unterstützen, um die lesbarsten Ergebnisse sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c17d8-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="c17d8-113">Windows 7 wurde um zwei neue Features mit hohem DPI-Anteil erweitert:</span><span class="sxs-lookup"><span data-stu-id="c17d8-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="c17d8-114">DPI-Einstellung pro Benutzer (bisher pro Computer)</span><span class="sxs-lookup"><span data-stu-id="c17d8-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="c17d8-115">DPI ohne Neustart ändern (Abmeldung/Anmeldung ist weiterhin erforderlich)</span><span class="sxs-lookup"><span data-stu-id="c17d8-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="c17d8-116">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="c17d8-116">Manifestation of Impact</span></span>

<span data-ttu-id="c17d8-117">Anwendungen, die den hohen DPI-Fall nicht verarbeiten, weisen wahrscheinlich visuelle Artefakte auf, z. B.:</span><span class="sxs-lookup"><span data-stu-id="c17d8-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="c17d8-118">Beschneiden der Benutzeroberfläche oder des Texts durch andere Benutzeroberflächenelemente</span><span class="sxs-lookup"><span data-stu-id="c17d8-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="c17d8-119">Inkonsistente Schriftgrade</span><span class="sxs-lookup"><span data-stu-id="c17d8-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="c17d8-120">Off-Screen-UIs</span><span class="sxs-lookup"><span data-stu-id="c17d8-120">Off-screen UIs</span></span>
-   <span data-ttu-id="c17d8-121">Weichzeichnen von Text oder Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c17d8-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="c17d8-122">Fehlerhafte Drag &amp; Drop-Eingaben oder andere Eingaben</span><span class="sxs-lookup"><span data-stu-id="c17d8-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="c17d8-123">Rendering von DX-Vollbildanwendungen teilweise außerhalb des Bildschirms</span><span class="sxs-lookup"><span data-stu-id="c17d8-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="c17d8-124">Lösung</span><span class="sxs-lookup"><span data-stu-id="c17d8-124">Solution</span></span>

<span data-ttu-id="c17d8-125">So sorgen Sie für DPI-fähige Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="c17d8-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="c17d8-126">Führen Sie einen funktionstüchtigen Testlauf auf hoher Ebene durch, einschließlich Installation und Deinstallation in den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="c17d8-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="c17d8-127">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c17d8-127">Setting</span></span>                                              | <span data-ttu-id="c17d8-128">Worauf Sie achten müssen</span><span class="sxs-lookup"><span data-stu-id="c17d8-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c17d8-129">1024 x 768 bei 120 DPI (125 % Skalierung)</span><span class="sxs-lookup"><span data-stu-id="c17d8-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="c17d8-130">Dies ist eine effektive Auflösung von ca. 800 x 600. Suchen Sie daher nach Benutzeroberflächenproblemen, die vom Bildschirm abgeschnitten wurden.</span><span class="sxs-lookup"><span data-stu-id="c17d8-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="c17d8-131">Suchen Sie auch nach pixilierten Bitmaps & Symbolen.</span><span class="sxs-lookup"><span data-stu-id="c17d8-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="c17d8-132">1600 x 1200 @144 DPI (150 % Skalierung)</span><span class="sxs-lookup"><span data-stu-id="c17d8-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="c17d8-133">Unscharfe Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c17d8-133">Blurry UI.</span></span> <span data-ttu-id="c17d8-134">Stellen Sie sicher, dass alle Mausvorgänge funktionieren, insbesondere drag & Drop-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c17d8-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="c17d8-135">Überprüfen Sie außerdem, ob die Vollbildmodi ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c17d8-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="c17d8-136">1600x1200 @ 144 DPI mit deaktivierter DPI-Virtualisierung</span><span class="sxs-lookup"><span data-stu-id="c17d8-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="c17d8-137">Häufig werden Schaltflächen und die Benutzeroberfläche nicht im Verhältnis zu größerem Text skaliert& es zu erheblichen Textausschneidefechen kommt.</span><span class="sxs-lookup"><span data-stu-id="c17d8-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="c17d8-138">Suchen Sie im Allgemeinen nach Layoutproblemen & pixilierten Bitmaten & Symbolen.</span><span class="sxs-lookup"><span data-stu-id="c17d8-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="c17d8-139">Notieren Sie sich alle gefundenen Probleme, einschließlich Standort, Bildschirmauflösung und DPI-Einstellungen, sowie das Verhalten der Anwendung in den anderen DPI-/Auflösungskonfigurationen aus Vollständigkeits-</span><span class="sxs-lookup"><span data-stu-id="c17d8-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="c17d8-140">Überprüfen Sie jedes Problem mit den allgemeinen DPI-Codierungsproblemen.</span><span class="sxs-lookup"><span data-stu-id="c17d8-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="c17d8-141">Bewerten der Kosten für die vollständige DPI-Wertung der Anwendung</span><span class="sxs-lookup"><span data-stu-id="c17d8-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="c17d8-142">Erstellen Sie eine Liste der erforderlichen Objekte mit hohem DPI-Werte (z. B. Schaltflächen, Symbole).</span><span class="sxs-lookup"><span data-stu-id="c17d8-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="c17d8-143">Arbeiten Sie die Liste der in Schritt 1 gefundenen DPI-Probleme durch, und beheben Sie sie.</span><span class="sxs-lookup"><span data-stu-id="c17d8-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="c17d8-144">Integrieren der neuen Ressourcen aus Schritt 5</span><span class="sxs-lookup"><span data-stu-id="c17d8-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="c17d8-145">Deklarieren Der DPI-bewusste Anwendung</span><span class="sxs-lookup"><span data-stu-id="c17d8-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="c17d8-146">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests</span><span class="sxs-lookup"><span data-stu-id="c17d8-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="c17d8-147">Führen Sie die DPI Awareness-Bewertung erneut aus, und überprüfen Sie, ob die Probleme behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="c17d8-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c17d8-148">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c17d8-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="c17d8-149">Desktopanwendungsentwicklung mit hohem DPI-Anteil unter Windows</span><span class="sxs-lookup"><span data-stu-id="c17d8-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="c17d8-150">**Kontakt für technische Fragen:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="c17d8-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
