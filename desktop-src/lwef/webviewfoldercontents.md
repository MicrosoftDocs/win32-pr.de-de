---
title: WebViewFolderContents-Objekt (Shldisp.h)
description: Wird von der Shell für die Verwendung in einer WebView implementiert.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung
- Webviewfoldercontents-Objekt, ältere Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339121"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="7712f-105">Webviewfoldercontents-Objekt</span><span class="sxs-lookup"><span data-stu-id="7712f-105">WebViewFolderContents object</span></span>

<span data-ttu-id="7712f-106">Wird von der Shell für die Verwendung in einer *WebView* implementiert.</span><span class="sxs-lookup"><span data-stu-id="7712f-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="7712f-107">**Webviewfoldercontents** wird automatisch mit dem aktuellen Ordner von WebView initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7712f-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="7712f-108">Es wird eine Shell-Ordneransicht erstellt, in der der Inhalt des Ordners in einem von fünf Formaten angezeigt wird: kleines Symbol, großes Symbol, Liste, Details und Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="7712f-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="7712f-109">Er ist außerhalb einer WebView ungültig.</span><span class="sxs-lookup"><span data-stu-id="7712f-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="7712f-110">Die von **webviewfoldercontents** verfügbar gemachten Methoden und Eigenschaften sind mit denen des [**shellfolderview**](/windows/desktop/shell/shellfolderview) -Objekts identisch.</span><span class="sxs-lookup"><span data-stu-id="7712f-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="7712f-111">Member</span><span class="sxs-lookup"><span data-stu-id="7712f-111">Members</span></span>

<span data-ttu-id="7712f-112">Das **webviewfoldercontents** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7712f-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="7712f-113">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7712f-113">Events</span></span>](#events)
-   [<span data-ttu-id="7712f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="7712f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="7712f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7712f-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="7712f-116">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7712f-116">Events</span></span>

<span data-ttu-id="7712f-117">Das **webviewfoldercontents** -Objekt enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="7712f-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="7712f-118">Ereignis</span><span class="sxs-lookup"><span data-stu-id="7712f-118">Event</span></span>                                                              | <span data-ttu-id="7712f-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7712f-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7712f-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="7712f-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="7712f-121">Tritt auf, wenn sich der Auswahl Zustand eines Elements oder der Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7712f-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="7712f-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="7712f-122">Methods</span></span>

<span data-ttu-id="7712f-123">Das **webviewfoldercontents** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7712f-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="7712f-124">Methode</span><span class="sxs-lookup"><span data-stu-id="7712f-124">Method</span></span>                                                       | <span data-ttu-id="7712f-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7712f-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7712f-126">**Popupitemmenu**</span><span class="sxs-lookup"><span data-stu-id="7712f-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="7712f-127">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7712f-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="7712f-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="7712f-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="7712f-129">Ruft ein [**folderitems**](../shell/folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="7712f-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="7712f-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="7712f-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="7712f-131">Legt den Auswahl Zustand eines Elements in der Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="7712f-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="7712f-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7712f-132">Properties</span></span>

<span data-ttu-id="7712f-133">Das **webviewfoldercontents** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7712f-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="7712f-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7712f-134">Property</span></span>                                                            | <span data-ttu-id="7712f-135">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7712f-135">Access type</span></span>          | <span data-ttu-id="7712f-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7712f-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7712f-137">**Application**</span><span class="sxs-lookup"><span data-stu-id="7712f-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="7712f-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7712f-138">Read-only</span></span><br/> | <span data-ttu-id="7712f-139">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7712f-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="7712f-140">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="7712f-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="7712f-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7712f-141">Read-only</span></span><br/> | <span data-ttu-id="7712f-142">Ruft ein [**folderItem**](../shell/folderitem.md) -Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="7712f-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="7712f-143">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="7712f-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="7712f-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7712f-144">Read-only</span></span><br/> | <span data-ttu-id="7712f-145">Ruft ein [**Ordner**](../shell/folder.md) Objekt ab, das die Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="7712f-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="7712f-146">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7712f-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="7712f-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7712f-147">Read-only</span></span><br/> | <span data-ttu-id="7712f-148">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7712f-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="7712f-149">**Skript**</span><span class="sxs-lookup"><span data-stu-id="7712f-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="7712f-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7712f-150">Read-only</span></span><br/> | <span data-ttu-id="7712f-151">Ruft das Skript Objekt für die Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="7712f-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="7712f-152">**Viewoptions**</span><span class="sxs-lookup"><span data-stu-id="7712f-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="7712f-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7712f-153">Read-only</span></span><br/> | <span data-ttu-id="7712f-154">Ruft einen Satz von [**shellfolderviewoptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) -Flags ab, die die aktuellen Optionen der Ansicht angeben.</span><span class="sxs-lookup"><span data-stu-id="7712f-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7712f-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7712f-155">Requirements</span></span>



| <span data-ttu-id="7712f-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7712f-156">Requirement</span></span> | <span data-ttu-id="7712f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="7712f-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7712f-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7712f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="7712f-159">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7712f-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7712f-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7712f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="7712f-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7712f-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7712f-162">Header</span><span class="sxs-lookup"><span data-stu-id="7712f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="7712f-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7712f-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7712f-164">IDL</span><span class="sxs-lookup"><span data-stu-id="7712f-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7712f-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7712f-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7712f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7712f-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7712f-167"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7712f-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

