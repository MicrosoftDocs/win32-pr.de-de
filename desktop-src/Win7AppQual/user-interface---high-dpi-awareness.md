---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354025"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="064c4-103">Benutzeroberfläche: Hohe DPI-Werte</span><span class="sxs-lookup"><span data-stu-id="064c4-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="064c4-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="064c4-104">Affected Platforms</span></span>

 <span data-ttu-id="064c4-105">**Clients** -Windows XP \| Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="064c4-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="064c4-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="064c4-106">Feature Impact</span></span>

<span data-ttu-id="064c4-107">**Schweregrad** -Mittel</span><span class="sxs-lookup"><span data-stu-id="064c4-107">**Severity** - Medium</span></span>  
<span data-ttu-id="064c4-108">**Frequency** -Medium</span><span class="sxs-lookup"><span data-stu-id="064c4-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="064c4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="064c4-109">Description</span></span>

<span data-ttu-id="064c4-110">Ziel ist es, Endbenutzern zu empfehlen, Ihre Anzeige auf die systemeigene Auflösung festzulegen und dpi anstelle der Bildschirmauflösung zu verwenden, um die Größe von angezeigter Text und Bilder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="064c4-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="064c4-111">Windows 7 kann eine Standard-dpi bei Neuinstallationen auf Computern, die von ihren OEMs mithilfe der DPI-Einstellungen konfiguriert wurden, automatisch erkennen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="064c4-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="064c4-112">Es gibt Tools, die Sie verwenden können, um Anwendungen zu entwerfen, die hoch dpi-fähig sind, um die gängigsten Ergebnisse sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="064c4-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="064c4-113">Wir haben Windows 7 zwei neue High-dpi-Features hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="064c4-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="064c4-114">DPI-Einstellung pro Benutzer (zuvor pro Computer)</span><span class="sxs-lookup"><span data-stu-id="064c4-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="064c4-115">DPI ohne Neustart ändern (Abmeldung/Anmeldung ist noch erforderlich)</span><span class="sxs-lookup"><span data-stu-id="064c4-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="064c4-116">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="064c4-116">Manifestation of Impact</span></span>

<span data-ttu-id="064c4-117">Anwendungen, die die Groß-/Kleinschreibung nicht verarbeiten, weisen wahrscheinlich visuelle Artefakte auf, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="064c4-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="064c4-118">Clipping von Benutzeroberfläche oder Text durch andere Benutzeroberflächen Elemente</span><span class="sxs-lookup"><span data-stu-id="064c4-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="064c4-119">Inkonsistente Schriftart Größen</span><span class="sxs-lookup"><span data-stu-id="064c4-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="064c4-120">Benutzerdefinierte Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="064c4-120">Off-screen UIs</span></span>
-   <span data-ttu-id="064c4-121">Verwischt von Text oder UI</span><span class="sxs-lookup"><span data-stu-id="064c4-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="064c4-122">Unterbrochene Drag & Drop-Eingaben oder andere Eingaben</span><span class="sxs-lookup"><span data-stu-id="064c4-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="064c4-123">Rendering von voll Bild-DX-Anwendungen teilweise aus dem Bildschirm</span><span class="sxs-lookup"><span data-stu-id="064c4-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="064c4-124">Lösung</span><span class="sxs-lookup"><span data-stu-id="064c4-124">Solution</span></span>

<span data-ttu-id="064c4-125">So machen Sie Ihre Anwendungen mit dpi-Werten kompatibel:</span><span class="sxs-lookup"><span data-stu-id="064c4-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="064c4-126">Führen Sie einen Funktions Testdurchlauf auf hoher Ebene aus, einschließlich der Installation und Deinstallation unter den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="064c4-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="064c4-127">Einstellung</span><span class="sxs-lookup"><span data-stu-id="064c4-127">Setting</span></span>                                              | <span data-ttu-id="064c4-128">Was Sie suchen müssen</span><span class="sxs-lookup"><span data-stu-id="064c4-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="064c4-129">1024 x 768 @ 120 dpi (125% Skalierung)</span><span class="sxs-lookup"><span data-stu-id="064c4-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="064c4-130">Dies ist eine effektive Auflösung von ~ 800X600. Achten Sie also auf die Benutzeroberfläche, die auf dem Bildschirm oder auf Layoutprobleme abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="064c4-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="064c4-131">Suchen Sie auch nach pixilen Bitmaps & Symbolen.</span><span class="sxs-lookup"><span data-stu-id="064c4-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="064c4-132">1600x1200 @144 dpi (150% Skalierung)</span><span class="sxs-lookup"><span data-stu-id="064c4-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="064c4-133">Blurry-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="064c4-133">Blurry UI.</span></span> <span data-ttu-id="064c4-134">Überprüfen Sie, ob alle Maus Vorgänge funktionieren, insbesondere ziehen Sie & Drop-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="064c4-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="064c4-135">Überprüfen Sie auch, ob die Vollbildmodi ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="064c4-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="064c4-136">1600x1200 @ 144 dpi mit deaktivierter dpi-Virtualisierung</span><span class="sxs-lookup"><span data-stu-id="064c4-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="064c4-137">Häufig werden Schaltflächen und die Benutzeroberfläche nicht in Relation zu größerem Text skaliert, & ein signifikanter Text Clipping vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="064c4-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="064c4-138">Suchen Sie im Allgemeinen nach Layoutproblemen, & & Symbolen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="064c4-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="064c4-139">Notieren Sie sich alle gefundenen Probleme, einschließlich des Speicher Orts, der Bildschirmauflösung und der DPI-Einstellungen. Außerdem wird erläutert, wie sich die Anwendung in den anderen dpi/Resolution-Konfigurationen aus Gründen der Vollständigkeit verhält.</span><span class="sxs-lookup"><span data-stu-id="064c4-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="064c4-140">Überprüfen der einzelnen Probleme gegen häufige dpi-Codierungs Probleme</span><span class="sxs-lookup"><span data-stu-id="064c4-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="064c4-141">Bewerten der Kosten für die vollständige dpi-Erkennung der Anwendung</span><span class="sxs-lookup"><span data-stu-id="064c4-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="064c4-142">Erstellen Sie eine Liste der erforderlichen hohen dpi-Objekte (z. b. Schaltflächen, Symbole).</span><span class="sxs-lookup"><span data-stu-id="064c4-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="064c4-143">Arbeiten Sie durch, und korrigieren Sie die Liste der in Schritt 1 gefundenen dpi-Probleme.</span><span class="sxs-lookup"><span data-stu-id="064c4-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="064c4-144">Integrieren der neuen Assets aus Schritt 5</span><span class="sxs-lookup"><span data-stu-id="064c4-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="064c4-145">Deklarieren Sie Ihre Anwendung dpi-fähig</span><span class="sxs-lookup"><span data-stu-id="064c4-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="064c4-146">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="064c4-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="064c4-147">Führen Sie die dpi-Bewertung erneut aus, und überprüfen Sie, ob die Probleme behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="064c4-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="064c4-148">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="064c4-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="064c4-149">Hohe dpi-Entwicklung für Desktop Anwendungen unter Windows</span><span class="sxs-lookup"><span data-stu-id="064c4-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="064c4-150">**Wenden Sie sich für technische Fragen an:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="064c4-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
