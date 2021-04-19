---
description: Entwicklung der MUI-Unterstützung in Windows-Versionen
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Entwicklung der MUI-Unterstützung in Windows-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362548"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="52d30-103">Entwicklung der MUI-Unterstützung in Windows-Versionen</span><span class="sxs-lookup"><span data-stu-id="52d30-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="52d30-104">Vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52d30-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="52d30-105">Windows Vista und darüber hinaus</span><span class="sxs-lookup"><span data-stu-id="52d30-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="52d30-106">Ein sprach neutrales/MUI-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="52d30-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="52d30-107">Bereitstellungs Szenarien sind vollständig MUI-basiert</span><span class="sxs-lookup"><span data-stu-id="52d30-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="52d30-108">Bereitstellung mit einem Image</span><span class="sxs-lookup"><span data-stu-id="52d30-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="52d30-109">Verbessertes Wartungs Modell</span><span class="sxs-lookup"><span data-stu-id="52d30-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="52d30-110">MUI-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="52d30-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="52d30-111">Sprach Verwaltung</span><span class="sxs-lookup"><span data-stu-id="52d30-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="52d30-112">Ressourcen Behandlung</span><span class="sxs-lookup"><span data-stu-id="52d30-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="52d30-113">Vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52d30-113">Before Windows Vista</span></span>

<span data-ttu-id="52d30-114">Vor der Windows Vista-Version waren Windows mit einsprachigen Images ausgeliefert, was bedeutete, dass jede lokalisierte Version von Windows eine einzige Sprache für Ihre Benutzeroberfläche enthielt.</span><span class="sxs-lookup"><span data-stu-id="52d30-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="52d30-115">MUI war ein Add-on für die englische Version des Betriebssystems, und die mehrsprachigen Benutzeroberflächen Pakete konnten nur bestimmten englischen Windows-Versionen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="52d30-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="52d30-116">Bei der Installation unter der englischen Version von Windows erlaubte MUI die Benutzeroberflächen Sprache des Betriebssystems entsprechend den Einstellungen einzelner Benutzer für eine der unterstützten Sprachen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="52d30-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="52d30-117">Das MUI Pack Modell hat die MUI-Unterstützung für Anwendungen nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="52d30-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="52d30-118">Obwohl Entwickler mehrsprachige Anwendungen erstellen konnten, mussten Sie dafür eigene Mechanismen erstellen.</span><span class="sxs-lookup"><span data-stu-id="52d30-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="52d30-119">Windows Vista und darüber hinaus</span><span class="sxs-lookup"><span data-stu-id="52d30-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="52d30-120">Mit Windows Vista machte Microsoft bedeutende Investitionen in MUI.</span><span class="sxs-lookup"><span data-stu-id="52d30-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="52d30-121">Windows Vista wurde von Grund auf auf einer MUI-Plattform erstellt.</span><span class="sxs-lookup"><span data-stu-id="52d30-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="52d30-122">Obwohl dies ein wichtiger Fortschritt in der Windows-Lokalisierungsstrategie darstellt, ist es ein wichtiger Faktor für Microsoft, Windows in mehr Sprachen als je zuvor bereitzustellen. es ist vor allem eine gute Voraussetzung für Windows-Benutzer und-Kunden.</span><span class="sxs-lookup"><span data-stu-id="52d30-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="52d30-123">Ein sprach neutrales/MUI-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="52d30-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="52d30-124">Die meisten Windows Vista-Binärdateien sind MUI-konform, und ihre lokalisierbaren Daten werden getrennt vom Code gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52d30-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="52d30-125">Dies bietet Flexibilität, da jeweils unterschiedliche Sprach Daten hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="52d30-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="52d30-126">Bereitstellungs Szenarien sind vollständig MUI-basiert</span><span class="sxs-lookup"><span data-stu-id="52d30-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="52d30-127">Der Verpackungs-und Installations Entwurf von Windows Vista ist MUI-basiert, und alle lokalisierbaren Daten werden in sprachspezifischen Paketen verpackt, und die einzelnen Sprachpakete können in verschiedenen Szenarien bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="52d30-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="52d30-128">Obwohl die Einzelhandels-DVDs für Windows Vista einzelne Sprachversionen enthalten, können Benutzer der Ultimate-Edition zusätzliche MUI Language Packs herunterladen und die Benutzeroberflächen Sprache über die Systemsteuerung für Regions **-und Sprachoptionen** wechseln.</span><span class="sxs-lookup"><span data-stu-id="52d30-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="52d30-129">Lizenznehmer von Enterprise Edition erhalten alle Sprachen und können diese bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52d30-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="52d30-130">Bereitstellung mit einem Image</span><span class="sxs-lookup"><span data-stu-id="52d30-130">Single image deployment</span></span>

<span data-ttu-id="52d30-131">Unternehmenskunden und-OEMs können nun die Anzahl der abzurufenden Images reduzieren, um Windows und Anwendungen auf Computern über verschiedene Gebiets Schemas über eine Bereitstellung mit nur einem Image bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52d30-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="52d30-132">Mit MUI unter Windows Vista kann ein Bild, das mehrere Sprachen enthält, für beliebige Benutzer bereitgestellt werden, und Benutzer können Ihre eigenen bevorzugten Sprachen (innerhalb der Richtlinie) während des Setups oder die anfängliche "Standarddarstellung" mit dem Computer ermitteln.</span><span class="sxs-lookup"><span data-stu-id="52d30-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="52d30-133">Insbesondere können OEMs viele Benutzeroberflächen Sprachen auf Ihren neuen Computern ablegen, um Benutzern die Auswahl aus dem Begrüßungs Center zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="52d30-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="52d30-134">Daher wird von einem Bild mit mehreren Sprachpaketen eine Liste der verfügbaren Sprachen angezeigt, und Benutzer können eine der verfügbaren Sprachen auswählen.</span><span class="sxs-lookup"><span data-stu-id="52d30-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="52d30-135">Alle internationalen Einstellungen werden dann entsprechend der ausgewählten Sprache oder dem ausgewählten Gebiets Schema festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52d30-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="52d30-136">Verbessertes Wartungs Modell</span><span class="sxs-lookup"><span data-stu-id="52d30-136">Improved servicing model</span></span>

<span data-ttu-id="52d30-137">Das gleiche QFE-oder sicherheitsfixpaket kann nun auf allen Sprachsystemen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="52d30-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="52d30-138">Dies ist wichtig, da es einen schnelleren Trend der Sicherheitskorrekturen ermöglicht und es allen internationalen Benutzern ermöglicht wird, von der gleichen Zeit für alle Sicherheitskorrekturen zu profitieren.</span><span class="sxs-lookup"><span data-stu-id="52d30-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="52d30-139">MUI-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="52d30-139">MUI infrastructure</span></span>

<span data-ttu-id="52d30-140">Ab Windows Vista sind MUI-APIs verfügbar, mit denen Entwickler die MUI-Mechanismen für Ihre eigenen Anwendungen nutzen können, ohne benutzerdefinierte Logik für die Ressourcenverarbeitung und sprach Verwaltung erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="52d30-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="52d30-141">Sprach Verwaltung</span><span class="sxs-lookup"><span data-stu-id="52d30-141">Language management</span></span>

<span data-ttu-id="52d30-142">Grundlegende MUI-APIs, die Verwaltungsfunktionen für die Benutzeroberfläche bereitstellen, sind als Teil der MUI-Infrastruktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52d30-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="52d30-143">Um die verschiedenen Einstellungen der Benutzeroberflächen Sprache auf System-, Benutzer-und Anwendungsebene verwalten zu können, kombiniert MUI Sie intern zu einer einzigen priorisierten Liste.</span><span class="sxs-lookup"><span data-stu-id="52d30-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="52d30-144">MUI implementiert dann auf der Grundlage dieser priorisierten Liste einen Fall Back Mechanismus, der partielle Lokalisierungslösungen ermöglicht und Benutzern eine angemessene –, falls nicht gewünscht – Benutzeroberflächen Sprache bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="52d30-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="52d30-145">Beispielsweise kann ein System, auf dem die spanische Version von Windows Vista mit einem auf dem Basis Betriebssystem installierten Sprachschnittstellen Paket (Sync Language Interface Pack) ausgeführt wird, das folgende Verhalten unterstützen: das System versucht, seine Ressourcen zuerst in Katalanisch anzuzeigen. wenn diese Ressourcen nicht in Katalanisch verfügbar sind, sollten Sie dem Benutzer stattdessen spanische Ressourcen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52d30-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="52d30-146">Ressourcen Behandlung</span><span class="sxs-lookup"><span data-stu-id="52d30-146">Resource handling</span></span>

<span data-ttu-id="52d30-147">Mit der verbesserten MUI-Infrastruktur, die ab Windows Vista verfügbar ist, sind die meisten gängigen Ressourcen Technologien MUI-fähig.</span><span class="sxs-lookup"><span data-stu-id="52d30-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="52d30-148">In der folgenden Tabelle finden Sie weitere Informationen zur Unterstützung der Ressourcen Behandlung in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52d30-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52d30-149">Category</span><span class="sxs-lookup"><span data-stu-id="52d30-149">Category</span></span></th>
<th><span data-ttu-id="52d30-150">Support</span><span class="sxs-lookup"><span data-stu-id="52d30-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52d30-151">Unterstützte Ressourcentypen</span><span class="sxs-lookup"><span data-stu-id="52d30-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="52d30-152">Win32/nicht verwaltete Ressource:. DLL/. EXE/. OCX</span><span class="sxs-lookup"><span data-stu-id="52d30-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="52d30-153">Shell-bezogene Registrierungen</span><span class="sxs-lookup"><span data-stu-id="52d30-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="52d30-154">Verwaltungs bezogene Ressourcen: Ereignisprotokoll, Snap-in/MSC-Dateien</span><span class="sxs-lookup"><span data-stu-id="52d30-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="52d30-155">WMI: MOF/MFL</span><span class="sxs-lookup"><span data-stu-id="52d30-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="52d30-156">Gruppenrichtlinie: ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="52d30-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="52d30-157">Verwaltete Resources.dll</span><span class="sxs-lookup"><span data-stu-id="52d30-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52d30-158">Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="52d30-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="52d30-159">Für Win32: RC.exe, MUIRCT.exe und Visual Studio 2005 und höher</span><span class="sxs-lookup"><span data-stu-id="52d30-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52d30-160">Eingeschränkte Ressourcentyp Unterstützung</span><span class="sxs-lookup"><span data-stu-id="52d30-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="52d30-161">\*. chm-Hilfedateien</span><span class="sxs-lookup"><span data-stu-id="52d30-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



