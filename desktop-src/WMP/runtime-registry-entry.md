---
title: Registrierungseintrag zur Laufzeit
description: Registrierungseintrag zur Laufzeit
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player,Laufzeitregistrierungseinträge
- Windows Media Player,Dateierweiterungen
- Windows Media Player,Registrierung
- Registrierung, Dateinamenerweiterungen
- Registrierung, Laufzeiteinträge
- registry,settings for Windows Media Player
- Registrierungseinstellungen der Dateinamenerweiterung
- Laufzeitregistrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424109"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="6ca28-111">Registrierungseintrag zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="6ca28-111">Runtime Registry Entry</span></span>

<span data-ttu-id="6ca28-112">Wenn Windows Media Player eine benutzerdefinierte Dateinamenerweiterung findet, sucht sie nach einem Registrierungsunterschlüssel, der der Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ca28-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="6ca28-113">Der Unterschlüssel wird unter [File Name Extension Registry Settings (Registrierungseinstellungen für Dateinamenerweiterungen) beschrieben.](file-name-extension-registry-settings.md)</span><span class="sxs-lookup"><span data-stu-id="6ca28-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="6ca28-114">Einer der Registrierungseinträge, die unter dem Unterschlüssel der Erweiterung angezeigt werden können, ist der **Runtimeeintrag.**</span><span class="sxs-lookup"><span data-stu-id="6ca28-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="6ca28-115">Der **Eintrag Runtime** gibt die zugrunde liegende Technologie an, die Windows Media Player, um digitale Mediendateien mit der benutzerdefinierten Erweiterung wiedergibt oder zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6ca28-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="6ca28-116">Der **Eintrag Runtime** hat das folgende Formular.</span><span class="sxs-lookup"><span data-stu-id="6ca28-116">The **Runtime** entry has the following form.</span></span>



|   <span data-ttu-id="6ca28-117">Name</span><span class="sxs-lookup"><span data-stu-id="6ca28-117">Name</span></span>   |   <span data-ttu-id="6ca28-118">Typ</span><span class="sxs-lookup"><span data-stu-id="6ca28-118">Type</span></span>         |   <span data-ttu-id="6ca28-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6ca28-119">Value</span></span>                                                       |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="6ca28-120">Typ</span><span class="sxs-lookup"><span data-stu-id="6ca28-120">Runtime</span></span>  | <span data-ttu-id="6ca28-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6ca28-121">**REG\_DWORD**</span></span> | <span data-ttu-id="6ca28-122">Eine positive ganze Zahl, die die zugrunde liegende Technologie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ca28-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="6ca28-123">Der Wert des **Runtime-Eintrags** muss einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="6ca28-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="6ca28-124">**Wert (dezimal)**</span><span class="sxs-lookup"><span data-stu-id="6ca28-124">**Value (decimal)**</span></span> | <span data-ttu-id="6ca28-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ca28-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca28-126">6</span><span class="sxs-lookup"><span data-stu-id="6ca28-126">6</span></span>                   | <span data-ttu-id="6ca28-127">Rendern mit dem Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="6ca28-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="6ca28-128">7</span><span class="sxs-lookup"><span data-stu-id="6ca28-128">7</span></span>                   | <span data-ttu-id="6ca28-129">Rendern mit Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6ca28-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="6ca28-130">13</span><span class="sxs-lookup"><span data-stu-id="6ca28-130">13</span></span>                  | <span data-ttu-id="6ca28-131">Konvertieren Sie die Datei mithilfe des angegebenen Konvertierungs-Plug-Ins.</span><span class="sxs-lookup"><span data-stu-id="6ca28-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="6ca28-132">Erfordert Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="6ca28-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="6ca28-133">Die **Registrierungseintragswerte** 6 und 7 der Runtime werden von Windows Media Player 9er Serie und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ca28-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="6ca28-134">Der Wert 13 wird von Windows Media Player 11 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ca28-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ca28-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ca28-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ca28-136">**ConvertPluginCLSID-Unterschlüssel**</span><span class="sxs-lookup"><span data-stu-id="6ca28-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="6ca28-137">**Registrierungseinstellungen für die Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="6ca28-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




