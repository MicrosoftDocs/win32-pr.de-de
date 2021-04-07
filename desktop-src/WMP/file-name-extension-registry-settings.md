---
title: Registrierungs Einstellungen für die Dateinamenerweiterung
description: Registrierungs Einstellungen für die Dateinamenerweiterung
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player, Registrierung
- Windows Media Player, Dateinamen Erweiterungen
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712953"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="deddc-108">Registrierungs Einstellungen für die Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="deddc-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="deddc-109">Wenn Ihre digitalen Mediendateien ein benutzerdefiniertes Format aufweisen, können Sie Windows Media Player Informationen über Ihr benutzerdefiniertes Format bereitstellen, indem Sie Einträge in der Registrierung auf dem Computer des Benutzers platzieren.</span><span class="sxs-lookup"><span data-stu-id="deddc-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="deddc-110">Windows Media Player überprüft Ihre Registrierungseinträge, um zu bestimmen, wie die Dateien verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="deddc-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="deddc-111">In der folgenden Liste sind einige Möglichkeiten aufgeführt, mit denen Sie Registrierungseinträge erstellen können, die das benutzerdefinierte Mediendatei Format betreffen.</span><span class="sxs-lookup"><span data-stu-id="deddc-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="deddc-112">Erteilen Sie dem Player die Berechtigung, Ihre Dateien wiederzugeben, zu kopieren oder zu transcodieren.</span><span class="sxs-lookup"><span data-stu-id="deddc-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="deddc-113">Geben Sie die zugrunde liegende Technologie an, die der Player für die Wiedergabe Ihrer Dateien verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="deddc-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="deddc-114">Geben Sie an, wo die Dateien in der Bibliotheks Ansicht des Players angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="deddc-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="deddc-115">Geben Sie ein Plug-in an, das der Player verwenden soll, um die Dateien in ein Standardformat zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="deddc-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="deddc-116">Geben Sie einen MTP-Format Code (Media Transport Protocol) an, mit dem der Player feststellen kann, ob ein bestimmtes tragbares Gerät das Dateiformat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="deddc-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="deddc-117">Die meisten Einträge, die Sie bereitstellen, befinden sich unter einem Unterschlüssel, der der benutzerdefinierten Dateinamenerweiterung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="deddc-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="deddc-118">Sie können diesen Unterschlüssel in der Unterstruktur HKEY \_ local \_ Machine und in der HKEY \_ Current \_ User-Unterstruktur erstellen.</span><span class="sxs-lookup"><span data-stu-id="deddc-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="deddc-119">Windows Media Player sucht zuerst in der Unterstruktur des lokalen HKEY-Computers \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="deddc-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="deddc-120">Wenn er nicht finden kann, was er benötigt, sucht er in der aktuellen HKEY- \_ \_ Benutzer Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="deddc-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="deddc-121">Beachten Sie, dass jeder Code, der versucht, in die Registrierung auf dem Computer des Benutzers zu schreiben, in die HKEY-Unterstruktur des lokalen Computers schreiben kann, \_ \_ Wenn der aktuelle Benutzer über Administratorrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="deddc-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="deddc-122">Um Informationen über das benutzerdefinierte Dateiformat in die Unterstruktur des lokalen HKEY-Computers zu schreiben \_ \_ , erstellen Sie den folgenden Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="deddc-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="deddc-123">**HKEY \_ Lokale \_ Computer \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\** *CustomExtension*</span><span class="sxs-lookup"><span data-stu-id="deddc-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="deddc-124">Dabei ist *CustomExtension* die Dateinamenerweiterung, einschließlich des Punkt Trennzeichens (.).</span><span class="sxs-lookup"><span data-stu-id="deddc-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="deddc-125">Wenn beispielsweise die Erweiterung für Ihr benutzerdefiniertes Dateiformat. XYZ lautet, erstellen Sie den folgenden Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="deddc-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="deddc-126">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . XYZ**</span><span class="sxs-lookup"><span data-stu-id="deddc-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="deddc-127">Um Informationen über das benutzerdefinierte Dateiformat in die HKEY \_ Current \_ User-Teilstruktur zu schreiben, erstellen Sie den folgenden Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="deddc-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="deddc-128">**HKEY \_ Aktuelle \_ Benutzer \\ Software \\ Microsoft \\ Media Player \\ Player \\ Extensions \\** *CustomExtension*</span><span class="sxs-lookup"><span data-stu-id="deddc-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="deddc-129">Sie können einen oder mehrere der folgenden Einträge in den Unterschlüssel *CustomExtension* schreiben.</span><span class="sxs-lookup"><span data-stu-id="deddc-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="deddc-130">**Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="deddc-130">**Permissions**</span></span>
-   <span data-ttu-id="deddc-131">**Laufzeit**</span><span class="sxs-lookup"><span data-stu-id="deddc-131">**Runtime**</span></span>
-   <span data-ttu-id="deddc-132">**Formatcode**</span><span class="sxs-lookup"><span data-stu-id="deddc-132">**FormatCode**</span></span>

<span data-ttu-id="deddc-133">Um Konvertierungs-Plug-Ins für Ihr benutzerdefiniertes Mediendatei Format anzugeben, erstellen Sie einen **convertpluginclsid** -Unterschlüssel in Ihrem *CustomExtension* -Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="deddc-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="deddc-134">Um anzugeben, wo Windows Media Player die Dateien in der Bibliotheks Ansicht anzeigen soll, schreiben Sie einen Eintrag, der das benutzerdefinierte Dateiformat im folgenden Unterschlüssel darstellt.</span><span class="sxs-lookup"><span data-stu-id="deddc-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="deddc-135">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Media Player \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="deddc-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="deddc-136">In den folgenden Themen werden die Registrierungs Unterschlüssel und-Einträge beschrieben, die Windows-Media Player Informationen zu benutzerdefinierten Mediendatei Formaten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="deddc-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="deddc-137">Registrierungs Eintrag für Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="deddc-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="deddc-138">Registrierungs Eintrag für die Laufzeit</span><span class="sxs-lookup"><span data-stu-id="deddc-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="deddc-139">Registrierungs Eintrag "Formatcode"</span><span class="sxs-lookup"><span data-stu-id="deddc-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="deddc-140">Registrierungseinträge für die Bibliotheks Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="deddc-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="deddc-141">Convertpluginclsid-Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="deddc-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="deddc-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="deddc-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deddc-143">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="deddc-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="deddc-144">**Windows Media Player-Konvertierungs-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="deddc-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




