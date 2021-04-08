---
title: Settings-Objekt (Windows Media Player SDK)
description: Das Settings-Objekt bietet eine Möglichkeit, verschiedene Einstellungen für Windows-Media Player mithilfe der folgenden Eigenschaften und Methoden zu ändern.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Einstellungs Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "103857740"
---
# <a name="settings-object"></a><span data-ttu-id="e4dad-104">Einstellungs Objekt</span><span class="sxs-lookup"><span data-stu-id="e4dad-104">Settings Object</span></span>

<span data-ttu-id="e4dad-105">Das **Settings** -Objekt bietet eine Möglichkeit, verschiedene Einstellungen für Windows-Media Player mithilfe der folgenden Eigenschaften und Methoden zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e4dad-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="e4dad-106">Das **Einstellungs** Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4dad-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="e4dad-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4dad-107">Property</span></span>                                                  | <span data-ttu-id="e4dad-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4dad-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4dad-109">Autostart</span><span class="sxs-lookup"><span data-stu-id="e4dad-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="e4dad-110">Gibt einen Wert an, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="e4dad-111">Schwebe</span><span class="sxs-lookup"><span data-stu-id="e4dad-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="e4dad-112">Gibt den aktuellen Stereo Saldo an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="e4dad-113">Basis</span><span class="sxs-lookup"><span data-stu-id="e4dad-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="e4dad-114">Gibt die Basis-URL an, die für die relative Pfad Auflösung mit in Mediendateien eingebetteten URL-Skript Befehlen verwendet wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="e4dad-115">defaultaudiolanguage</span><span class="sxs-lookup"><span data-stu-id="e4dad-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="e4dad-116">Ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der in Windows Media Player angegebenen Standard Audiosprache ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="e4dad-117">defaultframe</span><span class="sxs-lookup"><span data-stu-id="e4dad-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="e4dad-118">Gibt den Namen des Frames an oder ruft ihn ab, der zum Anzeigen einer URL verwendet wird, die in einem **ScriptCommand** -Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="e4dad-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="e4dad-119">enableerrordialogfelder</span><span class="sxs-lookup"><span data-stu-id="e4dad-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="e4dad-120">Gibt einen Wert an, der angibt, ob Fehler Dialogfelder automatisch angezeigt werden, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="e4dad-121">invokeurls</span><span class="sxs-lookup"><span data-stu-id="e4dad-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="e4dad-122">Gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft diesen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="e4dad-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="e4dad-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="e4dad-124">Ruft ab, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4dad-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="e4dad-125">mediaaccessrights</span><span class="sxs-lookup"><span data-stu-id="e4dad-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="e4dad-126">Ruft einen Wert ab, der die Rechte angibt, die derzeit für den Bibliotheks Zugriff gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="e4dad-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="e4dad-127">verstum</span><span class="sxs-lookup"><span data-stu-id="e4dad-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="e4dad-128">Gibt einen Wert an, der angibt, ob Audiodaten stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e4dad-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="e4dad-129">playcount</span><span class="sxs-lookup"><span data-stu-id="e4dad-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="e4dad-130">Gibt an oder ruft die Häufigkeit ab, mit der ein Medien Element wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e4dad-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="e4dad-131">zinss</span><span class="sxs-lookup"><span data-stu-id="e4dad-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="e4dad-132">Gibt die aktuelle Wiedergabe Rate an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="e4dad-133">volume</span><span class="sxs-lookup"><span data-stu-id="e4dad-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="e4dad-134">Gibt das aktuelle Volume an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="e4dad-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="e4dad-135">Das **Settings** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="e4dad-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="e4dad-136">Methode</span><span class="sxs-lookup"><span data-stu-id="e4dad-136">Method</span></span>                                                            | <span data-ttu-id="e4dad-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4dad-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="e4dad-138">getMode</span><span class="sxs-lookup"><span data-stu-id="e4dad-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="e4dad-139">Bestimmt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e4dad-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="e4dad-140">requestmediaaccessrights</span><span class="sxs-lookup"><span data-stu-id="e4dad-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="e4dad-141">Fordert eine angegebene Zugriffsebene für die Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="e4dad-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="e4dad-142">setMode</span><span class="sxs-lookup"><span data-stu-id="e4dad-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="e4dad-143">Legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.</span><span class="sxs-lookup"><span data-stu-id="e4dad-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="e4dad-144">Der Zugriff auf das **Einstellungs** Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e4dad-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="e4dad-145">Object</span><span class="sxs-lookup"><span data-stu-id="e4dad-145">Object</span></span>                      | <span data-ttu-id="e4dad-146">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4dad-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="e4dad-147">Player</span><span class="sxs-lookup"><span data-stu-id="e4dad-147">Player</span></span>](player-object.md) | [<span data-ttu-id="e4dad-148">settings</span><span class="sxs-lookup"><span data-stu-id="e4dad-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="e4dad-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4dad-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4dad-150">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="e4dad-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




