---
title: Referenz zur Skin-Programmierung
description: Referenz zur Skin-Programmierung
ms.assetid: 914f6045-7252-4a06-a514-d31ef6d2d03b
keywords:
- Windows-Media Player, Skins
- Windows Media Player Skins, Programmier Referenz
- Skins, Programmier Referenz
- Referenz für Skins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30194f0048f4ef66cf32b7c5f3f94c2bd4e190ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708189"
---
# <a name="skin-programming-reference"></a><span data-ttu-id="436e4-107">Referenz zur Skin-Programmierung</span><span class="sxs-lookup"><span data-stu-id="436e4-107">Skin Programming Reference</span></span>

<span data-ttu-id="436e4-108">Die Referenz zur Skin-Programmierung dokumentiert die folgenden Elemente und ihre zugeordneten Attribute, Methoden und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="436e4-108">The Skin Programming Reference documents the following elements and their associated attributes, methods, and events.</span></span>

<span data-ttu-id="436e4-109">Die Elemente und Attribute in diesem Abschnitt erfordern Windows Media Player 7,0 oder höher, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="436e4-109">The elements and attributes in this section require Windows Media Player 7.0 or later unless otherwise noted.</span></span>



| <span data-ttu-id="436e4-110">Element</span><span class="sxs-lookup"><span data-stu-id="436e4-110">Element</span></span>                                                  | <span data-ttu-id="436e4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="436e4-111">Description</span></span>                                                                         |
|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="436e4-112">Ambient-Attribute</span><span class="sxs-lookup"><span data-stu-id="436e4-112">Ambient Attributes</span></span>](ambient-attributes.md)             | <span data-ttu-id="436e4-113">Attribute, die für alle Skin-Elemente gelten, bei denen Ausnahmen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="436e4-113">Attributes that apply to all skin elements with exceptions noted.</span></span>                   |
| [<span data-ttu-id="436e4-114">Ambient-Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="436e4-114">Ambient Event Handlers</span></span>](ambient-event-handlers.md)     | <span data-ttu-id="436e4-115">Ereignishandler, die von den meisten Skin-Elementen implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="436e4-115">Event handlers that can be implemented by most skin elements.</span></span>                       |
| [<span data-ttu-id="436e4-116">Ambient-Ereignis Attribute</span><span class="sxs-lookup"><span data-stu-id="436e4-116">Ambient Event Attributes</span></span>](ambient-event-attributes.md) | <span data-ttu-id="436e4-117">Attribute, die den Zustand von Windows Media Player, wenn ein Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="436e4-117">Attributes detailing the state of Windows Media Player when an event is fired.</span></span>      |
| [<span data-ttu-id="436e4-118">Automu</span><span class="sxs-lookup"><span data-stu-id="436e4-118">AUTOMENU</span></span>](automenu-element.md)                         | <span data-ttu-id="436e4-119">Bietet eine Möglichkeit, den Bereich für den schnell Zugriff in einer Skin anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="436e4-119">Provides a way to display the Quick Access Panel in a skin.</span></span>                         |
| [<span data-ttu-id="436e4-120">Gedrückt</span><span class="sxs-lookup"><span data-stu-id="436e4-120">BUTTON</span></span>](button-element.md)                             | <span data-ttu-id="436e4-121">Eine eigenständige Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="436e4-121">A standalone button.</span></span>                                                                |
| [<span data-ttu-id="436e4-122">ButtonElement</span><span class="sxs-lookup"><span data-stu-id="436e4-122">BUTTONELEMENT</span></span>](buttonelement-element.md)               | <span data-ttu-id="436e4-123">Eine Schaltfläche in einer Schaltflächen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="436e4-123">A button within a button group.</span></span>                                                     |
| [<span data-ttu-id="436e4-124">Button Group</span><span class="sxs-lookup"><span data-stu-id="436e4-124">BUTTONGROUP</span></span>](buttongroup-element.md)                   | <span data-ttu-id="436e4-125">Eine Gruppe von Schaltflächen Elementen.</span><span class="sxs-lookup"><span data-stu-id="436e4-125">A group of button elements.</span></span>                                                         |
| [<span data-ttu-id="436e4-126">COLUMN</span><span class="sxs-lookup"><span data-stu-id="436e4-126">COLUMN</span></span>](column-element.md)                             | <span data-ttu-id="436e4-127">Stellt eine Spalte in einem Wiedergabelisten-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="436e4-127">Represents a column within a playlist control.</span></span>                                      |
| [<span data-ttu-id="436e4-128">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="436e4-128">CONTROLS</span></span>](controls-element.md)                         | <span data-ttu-id="436e4-129">Ermöglicht [den Zugriff](controls-object.md) auf das Steuerelement Objekt innerhalb eines Skin.</span><span class="sxs-lookup"><span data-stu-id="436e4-129">Provides access to the [Controls](controls-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="436e4-130">Customslider</span><span class="sxs-lookup"><span data-stu-id="436e4-130">CUSTOMSLIDER</span></span>](customslider-element.md)                 | <span data-ttu-id="436e4-131">Ein anpassbares Slider-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="436e4-131">A customizable slider control.</span></span>                                                      |
| [<span data-ttu-id="436e4-132">EDITBOX</span><span class="sxs-lookup"><span data-stu-id="436e4-132">EDITBOX</span></span>](editbox-element.md)                           | <span data-ttu-id="436e4-133">Bietet Benutzern die Möglichkeit, Text in einem Skin einzugeben.</span><span class="sxs-lookup"><span data-stu-id="436e4-133">Provides a way for users to enter text within a skin.</span></span>                               |
| [<span data-ttu-id="436e4-134">Einflüssen</span><span class="sxs-lookup"><span data-stu-id="436e4-134">EFFECTS</span></span>](effects-element.md)                           | <span data-ttu-id="436e4-135">Ein Element, das eine Auflistung von Effekten enthält und steuert.</span><span class="sxs-lookup"><span data-stu-id="436e4-135">An element that contains and controls a collection of effects.</span></span>                      |
| [<span data-ttu-id="436e4-136">Ausgleichs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="436e4-136">EQUALIZERSETTINGS</span></span>](equalizersettings-element.md)       | <span data-ttu-id="436e4-137">Ein Element, das die Bearbeitung des Grafik Ausgleichs ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="436e4-137">An element allowing manipulation of the graphic equalizer.</span></span>                          |
| [<span data-ttu-id="436e4-138">Position</span><span class="sxs-lookup"><span data-stu-id="436e4-138">ITEM</span></span>](item-element.md)                                 | <span data-ttu-id="436e4-139">Stellt ein Element in einem Listenfeld oder Popup Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="436e4-139">Represents an item in a list box or pop-up control.</span></span>                                 |
| [<span data-ttu-id="436e4-140">ListBox</span><span class="sxs-lookup"><span data-stu-id="436e4-140">LISTBOX</span></span>](listbox-element.md)                           | <span data-ttu-id="436e4-141">Bietet Benutzern die Möglichkeit, Elemente aus einer Liste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="436e4-141">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="436e4-142">Feldspieler</span><span class="sxs-lookup"><span data-stu-id="436e4-142">PLAYER</span></span>](player-element.md)                             | <span data-ttu-id="436e4-143">Ermöglicht den Zugriff auf das [Player](player-object.md) -Objekt aus einem Skin.</span><span class="sxs-lookup"><span data-stu-id="436e4-143">Provides access to the [Player](player-object.md) object from within a skin.</span></span>       |
| [<span data-ttu-id="436e4-144">Abspielen</span><span class="sxs-lookup"><span data-stu-id="436e4-144">PLAYLIST</span></span>](playlist-element.md)                         | <span data-ttu-id="436e4-145">Ein Element zum Steuern der Darstellung einer Wiedergabeliste innerhalb eines Skin.</span><span class="sxs-lookup"><span data-stu-id="436e4-145">An element for controlling the appearance of a playlist within a skin.</span></span>              |
| [<span data-ttu-id="436e4-146">Up</span><span class="sxs-lookup"><span data-stu-id="436e4-146">POPUP</span></span>](popup-element.md)                               | <span data-ttu-id="436e4-147">Bietet Benutzern die Möglichkeit, Elemente aus einer Liste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="436e4-147">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="436e4-148">PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="436e4-148">PROGRESSBAR</span></span>](progressbar-element.md)                   | <span data-ttu-id="436e4-149">Bietet eine Möglichkeit zum Anzeigen von Statusinformationen in einem horizontalen oder vertikalen Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="436e4-149">Provides a way to display progress information in a horizontal or vertical control.</span></span> |
| [<span data-ttu-id="436e4-150">EINSTELLUNGEN</span><span class="sxs-lookup"><span data-stu-id="436e4-150">SETTINGS</span></span>](settings-element.md)                         | <span data-ttu-id="436e4-151">Ermöglicht den Zugriff auf das [Einstellungs](settings-object.md) Objekt innerhalb eines Skin.</span><span class="sxs-lookup"><span data-stu-id="436e4-151">Provides access to the [Settings](settings-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="436e4-152">Keits</span><span class="sxs-lookup"><span data-stu-id="436e4-152">SLIDER</span></span>](slider-element.md)                             | <span data-ttu-id="436e4-153">Ein Schieberegler-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="436e4-153">A slider control.</span></span>                                                                   |
| [<span data-ttu-id="436e4-154">Unter Ansicht</span><span class="sxs-lookup"><span data-stu-id="436e4-154">SUBVIEW</span></span>](subview-element.md)                           | <span data-ttu-id="436e4-155">Unterabschnitte innerhalb einer Sicht, die verschoben oder ausgeblendet werden können.</span><span class="sxs-lookup"><span data-stu-id="436e4-155">Subsections within a view that can be moved or hidden.</span></span>                              |
| [<span data-ttu-id="436e4-156">Text</span><span class="sxs-lookup"><span data-stu-id="436e4-156">TEXT</span></span>](text-element.md)                                 | <span data-ttu-id="436e4-157">Ein Steuerelement, das Text enthält.</span><span class="sxs-lookup"><span data-stu-id="436e4-157">A control containing text.</span></span>                                                          |
| [<span data-ttu-id="436e4-158">Titel</span><span class="sxs-lookup"><span data-stu-id="436e4-158">THEME</span></span>](theme-element.md)                               | <span data-ttu-id="436e4-159">Das Hauptelement, das eine Skin-Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="436e4-159">The main element identifying a skin file.</span></span>                                           |
| [<span data-ttu-id="436e4-160">Video</span><span class="sxs-lookup"><span data-stu-id="436e4-160">VIDEO</span></span>](video-element.md)                               | <span data-ttu-id="436e4-161">Ein Element zum Angeben der Darstellung eines Videofensters.</span><span class="sxs-lookup"><span data-stu-id="436e4-161">An element for specifying the appearance of a video window.</span></span>                         |
| [<span data-ttu-id="436e4-162">Videosettings</span><span class="sxs-lookup"><span data-stu-id="436e4-162">VIDEOSETTINGS</span></span>](videosettings-element.md)               | <span data-ttu-id="436e4-163">Ein Element, das die Steuerung verschiedener Videoeinstellungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="436e4-163">An element allowing control of various video settings.</span></span>                              |
| [<span data-ttu-id="436e4-164">VIEW</span><span class="sxs-lookup"><span data-stu-id="436e4-164">VIEW</span></span>](view-element.md)                                 | <span data-ttu-id="436e4-165">Gibt an, wie die Benutzeroberfläche (User Interface, UI) für die einzelnen Medienkategorien aussieht.</span><span class="sxs-lookup"><span data-stu-id="436e4-165">Specifies what the user interface (UI) looks like for each category of media.</span></span>       |
| [<span data-ttu-id="436e4-166">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="436e4-166">Miscellaneous</span></span>](miscellaneous.md)                       | <span data-ttu-id="436e4-167">Spezialisierte Attribute und andere verschiedene Themen, die zum Erstellen von Skins verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="436e4-167">Specialized attributes and other miscellaneous topics for use in creating skins.</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="436e4-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="436e4-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="436e4-169">**Windows Media Player Skins**</span><span class="sxs-lookup"><span data-stu-id="436e4-169">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




