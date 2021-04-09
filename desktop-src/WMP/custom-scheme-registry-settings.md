---
title: Registrierungs Einstellungen für benutzerdefinierte Schemas
description: Registrierungs Einstellungen für benutzerdefinierte Schemas
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, Registrierungs Einstellungen für benutzerdefinierte Schemas
- Windows Media Player, Schemas
- Windows Media Player, Registrierung
- Registrierung, benutzerdefinierte Schema Einstellungen
- Registrierung, Schemas
- Registrierung, Einstellungen für Windows-Media Player
- Schemas
- Registrierungs Einstellungen für benutzerdefinierte Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036552"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="71b96-111">Registrierungs Einstellungen für benutzerdefinierte Schemas</span><span class="sxs-lookup"><span data-stu-id="71b96-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="71b96-112">Schemas sind benutzerdefinierte Protokolle.</span><span class="sxs-lookup"><span data-stu-id="71b96-112">Schemes are custom protocols.</span></span> <span data-ttu-id="71b96-113">Windows Media Player verwaltet eine Liste der Schemas in der Registrierung auf dem Computer des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="71b96-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="71b96-114">Wenn der Benutzer versucht, eine digitale Mediendatei wiederzugeben, prüft der Spieler zunächst, ob das Windows Media Format SDK das Schema unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71b96-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="71b96-115">Wenn dies nicht der Fall ist, überprüft der Spieler das Schema anhand der Liste in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="71b96-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="71b96-116">Wenn eine Entsprechung gefunden wird, überprüft der Spieler einen Wert, der angibt, welche zugrunde liegende Technologie oder *Laufzeit* (z. b. Microsoft DirectShow oder das Windows Media Format SDK) verwendet werden kann, um die Datei wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="71b96-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="71b96-117">Wenn keine Entsprechung gefunden wird, wird dem Benutzer ein Warn Dialogfeld angezeigt, in dem der Benutzer zur Eingabe der Berechtigung aufgefordert wird, die Datei wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="71b96-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="71b96-118">Wenn Sie digitale Mediendateien mit einem benutzerdefinierten Protokoll Schema streamen, können Sie verhindern, dass diese Warnung auf dem Computer des Benutzers angezeigt wird, indem Sie das Schema registrieren und einen Wert für die Laufzeit bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="71b96-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="71b96-119">Die Liste der Schemas wird als Satz von Registrierungs Schlüsseln verwaltet, die den registrierten Schemas entsprechen, ohne den Doppelpunkt und die beiden Schrägstriche (://).</span><span class="sxs-lookup"><span data-stu-id="71b96-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="71b96-120">Beispielsweise wird der Schlüssel für das wmhtml://-Schema, das zum Streamen von Rich-Media-Daten verwendet wird, als "wmhtml" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="71b96-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="71b96-121">Für den lokalen Computer und für jeden Benutzer wird eine separate Liste beibehalten.</span><span class="sxs-lookup"><span data-stu-id="71b96-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="71b96-122">Die Schema Schlüssel für den lokalen Computer sind Unterschlüssel des folgenden Registrierungsschlüssels:</span><span class="sxs-lookup"><span data-stu-id="71b96-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="71b96-123">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Schemas\\**</span><span class="sxs-lookup"><span data-stu-id="71b96-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="71b96-124">Der Schlüssel für das wmhtml://-Schema für den lokalen Computer lautet beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71b96-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="71b96-125">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Schemas \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="71b96-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="71b96-126">Um Werte in diesem Schlüssel zu ändern oder um einen neuen Unterschlüssel zu erstellen, muss der aktuelle Benutzer ein Administrator für den Computer sein.</span><span class="sxs-lookup"><span data-stu-id="71b96-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="71b96-127">Für einzelne Benutzer sind die Schema Schlüssel Unterschlüssel des folgenden Registrierungsschlüssels:</span><span class="sxs-lookup"><span data-stu-id="71b96-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="71b96-128">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Player \\ Schemas\\**</span><span class="sxs-lookup"><span data-stu-id="71b96-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="71b96-129">Der Schlüssel für das wmhtml://-Schema für den aktuellen Benutzer lautet z. b.:</span><span class="sxs-lookup"><span data-stu-id="71b96-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="71b96-130">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Player \\ Schemas \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="71b96-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="71b96-131">Bei der Überprüfung auf registrierte Schemas prüft der Spieler zunächst die Werte auf dem **lokalen HKEY- \_ \_ Computer**.</span><span class="sxs-lookup"><span data-stu-id="71b96-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="71b96-132">Wenn keine für das aktuelle Schema gefunden wird, überprüft der Spieler die Werte im **aktuellen HKEY \_ - \_ Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="71b96-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="71b96-133">Wenn keine für das aktuelle Schema gefunden wird, zeigt der Player dem Benutzer die Warnung an.</span><span class="sxs-lookup"><span data-stu-id="71b96-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="71b96-134">Jeder Schema Unterschlüssel kann einen der folgenden möglichen Werte für die *Laufzeit* enthalten.</span><span class="sxs-lookup"><span data-stu-id="71b96-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="71b96-135">Wert</span><span class="sxs-lookup"><span data-stu-id="71b96-135">Value</span></span> | <span data-ttu-id="71b96-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71b96-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="71b96-137">6</span><span class="sxs-lookup"><span data-stu-id="71b96-137">6</span></span>     | <span data-ttu-id="71b96-138">Rendering mit dem Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="71b96-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="71b96-139">7</span><span class="sxs-lookup"><span data-stu-id="71b96-139">7</span></span>     | <span data-ttu-id="71b96-140">Rendering mithilfe von Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="71b96-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="71b96-141">Das Ändern des *Lauf* Zeit Werts für ein Schema, das vom Windows Media Format SDK unterstützt wird, hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="71b96-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="71b96-142">Der Player verwendet immer das SDK für den Windows Media-Format als Laufzeit für Schemas, die das Windows Media Format SDK unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71b96-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="71b96-143">Dieser Registrierungs Wert ermöglicht die Laufzeitkonfiguration für benutzerdefinierte Schemas.</span><span class="sxs-lookup"><span data-stu-id="71b96-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71b96-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71b96-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b96-145">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="71b96-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




