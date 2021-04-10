---
title: Design-Element
description: Design-Element
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player Skins, Theme-Element
- Skins, Theme-Element
- Design-Element
- Verweis für Skins, Theme-Element
- Elemente, Design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855760"
---
# <a name="theme-element"></a><span data-ttu-id="113b3-108">Design-Element</span><span class="sxs-lookup"><span data-stu-id="113b3-108">THEME Element</span></span>

<span data-ttu-id="113b3-109">Das **Designelement ist das Element** auf der übergeordneten Ebene eines Skin und enthält mindestens ein **Ansichts** Element, das wiederum alle anderen Elemente in einer Skin enthält.</span><span class="sxs-lookup"><span data-stu-id="113b3-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="113b3-110">Innerhalb von Skriptcode wird **auf das Design** Element über das **globale Design** -Attribut und nicht über einen durch ein **ID** -Attribut angegebenen Namen zugegriffen, der vom Design **-Element nicht** unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="113b3-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="113b3-111">Das **Theme** -Element unterstützt die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="113b3-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="113b3-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="113b3-112">Attribute</span></span>                                | <span data-ttu-id="113b3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="113b3-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="113b3-114">Schrift</span><span class="sxs-lookup"><span data-stu-id="113b3-114">author</span></span>](theme-author.md)               | <span data-ttu-id="113b3-115">Gibt den Namen des Autors der Skin an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="113b3-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="113b3-116">authorversion</span><span class="sxs-lookup"><span data-stu-id="113b3-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="113b3-117">Gibt die vom Autor zugewiesene Versionsnummer der Skin an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="113b3-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="113b3-118">Copyright</span><span class="sxs-lookup"><span data-stu-id="113b3-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="113b3-119">Gibt die Copyright Zeichenfolge für die Skin an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="113b3-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="113b3-120">currentViewID</span><span class="sxs-lookup"><span data-stu-id="113b3-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="113b3-121">Gibt die aktuell angezeigte **Ansicht** an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="113b3-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="113b3-122">title</span><span class="sxs-lookup"><span data-stu-id="113b3-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="113b3-123">Gibt den Titel der Skin an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="113b3-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="113b3-124">version</span><span class="sxs-lookup"><span data-stu-id="113b3-124">version</span></span>](theme-version.md)             | <span data-ttu-id="113b3-125">Gibt die Windows Media Player-Versionsnummer an, für die die Skin erstellt wurde, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="113b3-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="113b3-126">Kann nur zur Entwurfszeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="113b3-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="113b3-127">Das **Theme** -Element unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="113b3-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="113b3-128">Methode</span><span class="sxs-lookup"><span data-stu-id="113b3-128">Method</span></span>                                         | <span data-ttu-id="113b3-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="113b3-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="113b3-130">Close View</span><span class="sxs-lookup"><span data-stu-id="113b3-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="113b3-131">Schließt eine geöffnete **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="113b3-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="113b3-132">loadpreference</span><span class="sxs-lookup"><span data-stu-id="113b3-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="113b3-133">Lädt eine Präferenz aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="113b3-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="113b3-134">logstring</span><span class="sxs-lookup"><span data-stu-id="113b3-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="113b3-135">Protokolliert eine benutzerdefinierte Zeichenfolge in der Fehler Datei, wenn die Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="113b3-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="113b3-136">OpenDialog</span><span class="sxs-lookup"><span data-stu-id="113b3-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="113b3-137">Öffnet ein Datei Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="113b3-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="113b3-138">OpenView –</span><span class="sxs-lookup"><span data-stu-id="113b3-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="113b3-139">Öffnet eine **Ansicht** in einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="113b3-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="113b3-140">openviewrelative</span><span class="sxs-lookup"><span data-stu-id="113b3-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="113b3-141">Öffnet eine **Ansicht** in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.</span><span class="sxs-lookup"><span data-stu-id="113b3-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="113b3-142">PlaySound</span><span class="sxs-lookup"><span data-stu-id="113b3-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="113b3-143">Gibt die angegebene Audiodatei wieder.</span><span class="sxs-lookup"><span data-stu-id="113b3-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="113b3-144">savepreference</span><span class="sxs-lookup"><span data-stu-id="113b3-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="113b3-145">Speichert eine Einstellung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="113b3-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="113b3-146">showerrordialog</span><span class="sxs-lookup"><span data-stu-id="113b3-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="113b3-147">Zeigt das Dialogfeld Standardfehler an.</span><span class="sxs-lookup"><span data-stu-id="113b3-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="113b3-148">Das **Theme** -Element unterstützt keine Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="113b3-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="113b3-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="113b3-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="113b3-150">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="113b3-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




