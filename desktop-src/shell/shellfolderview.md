---
description: Stellt die Objekte in einer Ansicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Ansicht verwendet werden.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Shellfolderview-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994998"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="52558-103">Shellfolderview-Objekt</span><span class="sxs-lookup"><span data-stu-id="52558-103">ShellFolderView object</span></span>

<span data-ttu-id="52558-104">Stellt die Objekte in einer Ansicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Ansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52558-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="52558-105">Member</span><span class="sxs-lookup"><span data-stu-id="52558-105">Members</span></span>

<span data-ttu-id="52558-106">Das **shellfolderview** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52558-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="52558-107">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="52558-107">Events</span></span>](#events)
-   [<span data-ttu-id="52558-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="52558-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="52558-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52558-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="52558-110">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="52558-110">Events</span></span>

<span data-ttu-id="52558-111">Das **shellfolderview** -Objekt enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="52558-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="52558-112">Ereignis</span><span class="sxs-lookup"><span data-stu-id="52558-112">Event</span></span>                                                        | <span data-ttu-id="52558-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52558-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="52558-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="52558-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="52558-115">Tritt auf, wenn sich der Auswahl Zustand eines Elements oder der Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="52558-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="52558-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="52558-116">Methods</span></span>

<span data-ttu-id="52558-117">Das **shellfolderview** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52558-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="52558-118">Methode</span><span class="sxs-lookup"><span data-stu-id="52558-118">Method</span></span>                                                 | <span data-ttu-id="52558-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52558-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52558-120">**Popupitemmenu**</span><span class="sxs-lookup"><span data-stu-id="52558-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="52558-121">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="52558-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="52558-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="52558-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="52558-123">Ruft ein [**folderitems**](folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="52558-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="52558-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="52558-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="52558-125">Legt den Auswahl Zustand eines Elements in der Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="52558-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="52558-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52558-126">Properties</span></span>

<span data-ttu-id="52558-127">Das **shellfolderview** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52558-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="52558-128">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="52558-128">Property</span></span>                                                      | <span data-ttu-id="52558-129">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="52558-129">Access type</span></span>          | <span data-ttu-id="52558-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52558-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52558-131">**Application**</span><span class="sxs-lookup"><span data-stu-id="52558-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="52558-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52558-132">Read-only</span></span><br/> | <span data-ttu-id="52558-133">Enthält das Anwendungs Objekt des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="52558-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="52558-134">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="52558-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="52558-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52558-135">Read-only</span></span><br/> | <span data-ttu-id="52558-136">Ruft ein [**folderItem**](folderitem.md) -Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="52558-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="52558-137">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="52558-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="52558-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52558-138">Read-only</span></span><br/> | <span data-ttu-id="52558-139">Ruft ein [**Ordner**](folder.md) Objekt ab, das die Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="52558-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="52558-140">**Parent**</span><span class="sxs-lookup"><span data-stu-id="52558-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="52558-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52558-141">Read-only</span></span><br/> | <span data-ttu-id="52558-142">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="52558-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="52558-143">**Skript**</span><span class="sxs-lookup"><span data-stu-id="52558-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="52558-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52558-144">Read-only</span></span><br/> | <span data-ttu-id="52558-145">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="52558-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="52558-146">**Viewoptions**</span><span class="sxs-lookup"><span data-stu-id="52558-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="52558-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52558-147">Read-only</span></span><br/> | <span data-ttu-id="52558-148">Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.</span><span class="sxs-lookup"><span data-stu-id="52558-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="52558-149">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="52558-149">Requirements</span></span>



| <span data-ttu-id="52558-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52558-150">Requirement</span></span> | <span data-ttu-id="52558-151">Wert</span><span class="sxs-lookup"><span data-stu-id="52558-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52558-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52558-152">Minimum supported client</span></span><br/> | <span data-ttu-id="52558-153">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52558-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="52558-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52558-154">Minimum supported server</span></span><br/> | <span data-ttu-id="52558-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52558-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52558-156">Header</span><span class="sxs-lookup"><span data-stu-id="52558-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="52558-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="52558-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="52558-158">IDL</span><span class="sxs-lookup"><span data-stu-id="52558-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52558-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52558-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="52558-160">DLL</span><span class="sxs-lookup"><span data-stu-id="52558-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52558-161"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="52558-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="52558-162">IID</span><span class="sxs-lookup"><span data-stu-id="52558-162">IID</span></span><br/>                      | <span data-ttu-id="52558-163">CLSID \_ shellfolderview</span><span class="sxs-lookup"><span data-stu-id="52558-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="52558-164">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52558-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52558-165">**Shellfolderviewoptions-Flags**</span><span class="sxs-lookup"><span data-stu-id="52558-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




