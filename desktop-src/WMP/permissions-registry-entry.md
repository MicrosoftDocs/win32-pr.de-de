---
title: Registrierungs Eintrag für Berechtigungen
description: Registrierungs Eintrag für Berechtigungen
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Berechtigungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Berechtigungen
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038532"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="195e4-111">Registrierungs Eintrag für Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="195e4-111">Permissions Registry Entry</span></span>

<span data-ttu-id="195e4-112">Wenn Windows Media Player auf eine benutzerdefinierte Dateierweiterung trifft, sucht es nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="195e4-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="195e4-113">Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="195e4-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="195e4-114">Einer der Registrierungseinträge, der unter dem Unterschlüssel der Erweiterung angezeigt werden kann, ist der **Berechtigungs** Eintrag.</span><span class="sxs-lookup"><span data-stu-id="195e4-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="195e4-115">Der **Berechtigungs** Eintrag gibt die Aktionen an, die Windows Media Player für Dateien mit der benutzerdefinierten Erweiterung ausführen darf.</span><span class="sxs-lookup"><span data-stu-id="195e4-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="195e4-116">Der **Berechtigungs** Eintrag weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="195e4-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="195e4-117">Name</span><span class="sxs-lookup"><span data-stu-id="195e4-117">Name</span></span>        | <span data-ttu-id="195e4-118">type</span><span class="sxs-lookup"><span data-stu-id="195e4-118">Type</span></span>           | <span data-ttu-id="195e4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="195e4-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="195e4-120">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="195e4-120">Permissions</span></span> | <span data-ttu-id="195e4-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="195e4-121">**REG\_DWORD**</span></span> | <span data-ttu-id="195e4-122">Ein Satz von Flags, von denen jeder die Berechtigung für eine bestimmte Aktion erteilt.</span><span class="sxs-lookup"><span data-stu-id="195e4-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="195e4-123">Der Wert des **Berechtigungs** Eintrags ist ein bitweises **or** von einem oder mehreren der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="195e4-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="195e4-124">Flag (Dezimalwert)</span><span class="sxs-lookup"><span data-stu-id="195e4-124">Flag (decimal value)</span></span> | <span data-ttu-id="195e4-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="195e4-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="195e4-126">1</span><span class="sxs-lookup"><span data-stu-id="195e4-126">1</span></span>                    | <span data-ttu-id="195e4-127">Berechtigung für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="195e4-127">Permission for playback.</span></span> <span data-ttu-id="195e4-128">Dateien mit der registrierten Dateinamenerweiterung können wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="195e4-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="195e4-129">2</span><span class="sxs-lookup"><span data-stu-id="195e4-129">2</span></span>                    | <span data-ttu-id="195e4-130">Berechtigung zum Löschen des Ordners.</span><span class="sxs-lookup"><span data-stu-id="195e4-130">Permission for folder drop.</span></span> <span data-ttu-id="195e4-131">Dateien mit der registrierten Dateinamenerweiterung werden in die Wiedergabeliste eingeschlossen, die erstellt wird, wenn der Benutzer einen Ordner zieht, der die Dateien enthält, und ihn auf der Benutzeroberfläche des Players ablegen.</span><span class="sxs-lookup"><span data-stu-id="195e4-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="195e4-132">4</span><span class="sxs-lookup"><span data-stu-id="195e4-132">4</span></span>                    | <span data-ttu-id="195e4-133">Berechtigung für Medien-CD.</span><span class="sxs-lookup"><span data-stu-id="195e4-133">Permission for media CD.</span></span> <span data-ttu-id="195e4-134">Dateien mit der registrierten Dateinamenerweiterung werden in die Wiedergabeliste eingeschlossen, die erstellt wird, wenn eine CD, die die Dateien enthält, in das CD-ROM-Laufwerk eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="195e4-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="195e4-135">8</span><span class="sxs-lookup"><span data-stu-id="195e4-135">8</span></span>                    | <span data-ttu-id="195e4-136">Berechtigung für die Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="195e4-136">Permission for the library.</span></span> <span data-ttu-id="195e4-137">Dateien mit der Dateinamenerweiterung "registriert" können der Bibliothek hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="195e4-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="195e4-138">Erforderlich für Konvertierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="195e4-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="195e4-139">16</span><span class="sxs-lookup"><span data-stu-id="195e4-139">16</span></span>                   | <span data-ttu-id="195e4-140">Berechtigung für HTML-Streaming.</span><span class="sxs-lookup"><span data-stu-id="195e4-140">Permission for HTML streaming.</span></span> <span data-ttu-id="195e4-141">Dateien mit der registrierten Dateinamenerweiterung werden in den Internet Explorer-Cache eingefügt, wenn Sie von einem Webstream übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="195e4-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="195e4-142">128</span><span class="sxs-lookup"><span data-stu-id="195e4-142">128</span></span>                  | <span data-ttu-id="195e4-143">Berechtigung für die Transcodierung.</span><span class="sxs-lookup"><span data-stu-id="195e4-143">Permission for transcoding.</span></span> <span data-ttu-id="195e4-144">Dateien mit der registrierten Dateinamenerweiterung können unter bestimmten Bedingungen in das Windows Media-Format transcodiert werden.</span><span class="sxs-lookup"><span data-stu-id="195e4-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="195e4-145">Weitere Informationen finden Sie unter [iwmptranscodepolicy:: allowtranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span><span class="sxs-lookup"><span data-stu-id="195e4-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="195e4-146">Erfordert Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="195e4-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="195e4-147">Wenn der Benutzer versucht, eine Mediendatei mit einer benutzerdefinierten Dateinamenerweiterung wiederzugeben, sucht Windows Media Player nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="195e4-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="195e4-148">Wenn keine Entsprechung gefunden wird, wird dem Benutzer ein Warn Dialogfeld angezeigt, in dem der Benutzer zur Eingabe der Berechtigung aufgefordert wird, die Datei wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="195e4-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="195e4-149">Wenn Sie digitale Mediendateien mit benutzerdefinierten Dateinamen Erweiterungen erstellen, können Sie verhindern, dass diese Warnung auf dem Computer des Benutzers angezeigt wird, indem Sie die Dateinamenerweiterung registrieren und einen **Berechtigungs** Eintrag angeben.</span><span class="sxs-lookup"><span data-stu-id="195e4-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="195e4-150">Der **Berechtigungs** Eintrag (mit Ausnahme des Flagwerts 128) wird von der Windows Media Player 9-Serie und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="195e4-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="195e4-151">Der Flagwert 128 wird von Windows Media Player 10 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="195e4-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="195e4-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="195e4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="195e4-153">**Registrierungs Einstellungen für die Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="195e4-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




