---
title: Convertpluginclsid-Unterschlüssel
description: Convertpluginclsid-Unterschlüssel
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player, convertpluginclsid-Unterschlüssel
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, convertpluginclsid-Unterschlüssel
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Convertpluginclsid-Unterschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037055"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="cac63-111">Convertpluginclsid-Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="cac63-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="cac63-112">Wenn Windows Media Player 11 auf eine benutzerdefinierte Dateierweiterung stößt, sucht Sie nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="cac63-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="cac63-113">Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cac63-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="cac63-114">In einigen Fällen verfügt der Unterschlüssel der Erweiterung über einen Unterschlüssel namens **convertpluginclsid**.</span><span class="sxs-lookup"><span data-stu-id="cac63-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="cac63-115">Nehmen Sie beispielsweise an, Sie haben ein benutzerdefiniertes Dateiformat (mit der Dateinamenerweiterung. XYZ) und ein Konvertierungs-Plug-in erstellt, das die Dateien in ein von Windows unterstütztes Format konvertiert Media Player dann würden Sie die Klassen-ID des Plug-ins in einem oder beiden der folgenden untergeordneten Schlüssel speichern.</span><span class="sxs-lookup"><span data-stu-id="cac63-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="cac63-116">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . XYZ \\ convertpluginclsid**</span><span class="sxs-lookup"><span data-stu-id="cac63-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="cac63-117">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Player \\ Extensions \\ . XYZ \\ convertpluginclsid**</span><span class="sxs-lookup"><span data-stu-id="cac63-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="cac63-118">Der **convertpluginclsid** -Unterschlüssel gibt die Klassen-IDs von Plug-ins an, die von Windows Media Player verwendet werden können, um eine Mediendatei aus dem benutzerdefinierten Format in ein Format zu konvertieren, das vom Player unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cac63-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="cac63-119">Der **convertpluginclsid** -Unterschlüssel weist die folgenden Einträge auf.</span><span class="sxs-lookup"><span data-stu-id="cac63-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="cac63-120">Ein Standardeintrag, der das Standard Konvertierungs-Plug-in darstellt.</span><span class="sxs-lookup"><span data-stu-id="cac63-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="cac63-121">Ein benannter Eintrag, der das Standard Konvertierungs-Plug-in darstellt.</span><span class="sxs-lookup"><span data-stu-id="cac63-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="cac63-122">Zusätzliche benannte Einträge, die Alternative konvertierungsplug-ins darstellen.</span><span class="sxs-lookup"><span data-stu-id="cac63-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="cac63-123">Nehmen Sie beispielsweise an, ein benutzerdefiniertes Dateiformat verfügt über ein Standard Konvertierungs-Plug-in und zwei alternative Konvertierungs-Plug-ins. Die Registrierungseinträge unter dem **convertpluginclsid** -Unterschlüssel weisen die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="cac63-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="cac63-124">Name</span><span class="sxs-lookup"><span data-stu-id="cac63-124">Name</span></span>                                                                          | <span data-ttu-id="cac63-125">type</span><span class="sxs-lookup"><span data-stu-id="cac63-125">Type</span></span>        | <span data-ttu-id="cac63-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cac63-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="cac63-127">Standard</span><span class="sxs-lookup"><span data-stu-id="cac63-127">Default</span></span>                                                                       | <span data-ttu-id="cac63-128">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="cac63-128">**REG\_SZ**</span></span> | <span data-ttu-id="cac63-129">Die Klassen-ID des Standard Konvertierungs-Plug-ins im Registrierungs Format.</span><span class="sxs-lookup"><span data-stu-id="cac63-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="cac63-130">Die Klassen-ID des Standard Konvertierungs-Plug-ins im Registrierungs Format.</span><span class="sxs-lookup"><span data-stu-id="cac63-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="cac63-131">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="cac63-131">**REG\_SZ**</span></span> | <span data-ttu-id="cac63-132">Der Anzeige Name des Standard Konvertierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="cac63-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="cac63-133">Die Klassen-ID im Registrierungs Format des ersten alternativen Konvertierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="cac63-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="cac63-134">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="cac63-134">**REG\_SZ**</span></span> | <span data-ttu-id="cac63-135">Der Anzeige Name des ersten alternativen Konvertierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="cac63-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="cac63-136">Die Klassen-ID im Registrierungs Format des zweiten Alternativen Konvertierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="cac63-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="cac63-137">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="cac63-137">**REG\_SZ**</span></span> | <span data-ttu-id="cac63-138">Der Anzeige Name des zweiten Alternativen Konvertierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="cac63-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="cac63-139">Beachten Sie, dass das Standard Konvertierungs-Plug-in durch zwei Registrierungseinträge dargestellt wird: der Standardeintrag und ein benannter Eintrag.</span><span class="sxs-lookup"><span data-stu-id="cac63-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="cac63-140">Windows Media Player verwendet den Standardeintrag, um zu bestimmen, welches Plug-in das standardmäßige (primäre) Konvertierungs-Plug-in ist.</span><span class="sxs-lookup"><span data-stu-id="cac63-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="cac63-141">Windows Media Player verwendet die benannten Einträge zum Abrufen von anzeigen Amen für alle Konvertierungs-Plug-ins, einschließlich des Standard-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="cac63-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="cac63-142">Der Anzeige Name eines Konvertierungs-Plug-ins wird von dem Unternehmen bestimmt, das das Plug-in erstellt.</span><span class="sxs-lookup"><span data-stu-id="cac63-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="cac63-143">In Windows Media Player kann der Anzeige Name in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cac63-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="cac63-144">Wenn Windows Media Player versucht, eine Datei aus einem benutzerdefinierten Format in ein Standardformat zu konvertieren, wird zuerst das Standard-Plug-in geladen.</span><span class="sxs-lookup"><span data-stu-id="cac63-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="cac63-145">Wenn das Standard-Plug-in die Datei nicht konvertieren kann und die \_ Datei \_ Besitzer NS E WMP \_ Convert Plugin UNKNOWN zurückgibt \_ \_ \_ \_ , lädt der Player jedes Alternative Plug-in, bis eine erfolgreiche Konvertierung erfolgt, oder es sind keine weiteren Plug-ins zum ausprobieren vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cac63-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="cac63-146">Der Player zeigt keine Warnmeldung an, wenn kein Konvertierungs-Plug-in für die Dateinamenerweiterung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="cac63-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="cac63-147">Der Registrierungs Eintrag **convertpluginclsid** wird von Windows Media Player 11 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cac63-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cac63-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cac63-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac63-149">**Registrierungs Einstellungen für die Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="cac63-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="cac63-150">**Windows Media Player-Konvertierungs-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="cac63-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




