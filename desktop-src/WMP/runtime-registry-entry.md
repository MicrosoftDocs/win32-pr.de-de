---
title: Registrierungs Eintrag für die Laufzeit
description: Registrierungs Eintrag für die Laufzeit
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, Lauf Zeit Registrierungseinträge
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Lauf Zeiteinträge
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Registrierungseinträge für die Laufzeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037207"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="58373-111">Registrierungs Eintrag für die Laufzeit</span><span class="sxs-lookup"><span data-stu-id="58373-111">Runtime Registry Entry</span></span>

<span data-ttu-id="58373-112">Wenn Windows Media Player auf eine benutzerdefinierte Dateierweiterung trifft, sucht es nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="58373-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="58373-113">Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58373-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="58373-114">Einer der Registrierungseinträge, der unter dem Unterschlüssel der Erweiterung angezeigt werden kann, ist der **Lauf** Zeiteintrag.</span><span class="sxs-lookup"><span data-stu-id="58373-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="58373-115">Der **Lauf** Zeiteintrag gibt die zugrunde liegende Technologie an, mit der Windows Media Player digitale Mediendateien mit der benutzerdefinierten Erweiterung wiedergeben oder konvertieren kann.</span><span class="sxs-lookup"><span data-stu-id="58373-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="58373-116">Der **Lauf** Zeiteintrag weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="58373-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="58373-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="58373-117">**Name**</span></span> | <span data-ttu-id="58373-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="58373-118">**Type**</span></span>       | <span data-ttu-id="58373-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="58373-119">**Value**</span></span>                                                     |
| <span data-ttu-id="58373-120">Typ</span><span class="sxs-lookup"><span data-stu-id="58373-120">Runtime</span></span>  | <span data-ttu-id="58373-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="58373-121">**REG\_DWORD**</span></span> | <span data-ttu-id="58373-122">Eine positive ganze Zahl, die die zugrunde liegende Technologie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="58373-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="58373-123">Der Wert für den **Lauf** Zeiteintrag muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="58373-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="58373-124">**Wert (dezimal)**</span><span class="sxs-lookup"><span data-stu-id="58373-124">**Value (decimal)**</span></span> | <span data-ttu-id="58373-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58373-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="58373-126">6</span><span class="sxs-lookup"><span data-stu-id="58373-126">6</span></span>                   | <span data-ttu-id="58373-127">Rendering mit dem Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="58373-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="58373-128">7</span><span class="sxs-lookup"><span data-stu-id="58373-128">7</span></span>                   | <span data-ttu-id="58373-129">Rendering mithilfe von Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="58373-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="58373-130">13</span><span class="sxs-lookup"><span data-stu-id="58373-130">13</span></span>                  | <span data-ttu-id="58373-131">Konvertiert die Datei mit dem angegebenen Konvertierungs-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="58373-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="58373-132">Erfordert Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="58373-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="58373-133">Die **Lauf** Zeit Registrierungs Eintrags Werte 6 und 7 werden von der Windows Media Player 9-Serie und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58373-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="58373-134">Der Wert 13 wird von Windows Media Player 11 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58373-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58373-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58373-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58373-136">**Convertpluginclsid-Unterschlüssel**</span><span class="sxs-lookup"><span data-stu-id="58373-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="58373-137">**Registrierungs Einstellungen für die Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="58373-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




