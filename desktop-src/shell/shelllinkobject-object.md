---
description: Verwaltet shelllinks. Dieses Objekt stellt einen Großteil der Funktionen der IShellLink-Schnittstelle für Skript Anwendungen zur Verfügung.
title: Shelllinkobject-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980729"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="a49e4-104">Shelllinkobject-Objekt</span><span class="sxs-lookup"><span data-stu-id="a49e4-104">ShellLinkObject object</span></span>

<span data-ttu-id="a49e4-105">Verwaltet shelllinks.</span><span class="sxs-lookup"><span data-stu-id="a49e4-105">Manages Shell links.</span></span> <span data-ttu-id="a49e4-106">Dieses Objekt stellt einen Großteil der Funktionen der [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle für Skript Anwendungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a49e4-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="a49e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="a49e4-107">Members</span></span>

<span data-ttu-id="a49e4-108">Das **shelllinkobject** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a49e4-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="a49e4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a49e4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a49e4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49e4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a49e4-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a49e4-111">Methods</span></span>

<span data-ttu-id="a49e4-112">Das **shelllinkobject** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a49e4-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="a49e4-113">Methode</span><span class="sxs-lookup"><span data-stu-id="a49e4-113">Method</span></span>                                                     | <span data-ttu-id="a49e4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a49e4-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a49e4-115">**Getitirelocation**</span><span class="sxs-lookup"><span data-stu-id="a49e4-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="a49e4-116">Ruft den Speicherort des Symbols ab, das dem Link zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a49e4-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="a49e4-117">**Beheben**</span><span class="sxs-lookup"><span data-stu-id="a49e4-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="a49e4-118">Sucht das Ziel eines shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="a49e4-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="a49e4-119">**Sicher**</span><span class="sxs-lookup"><span data-stu-id="a49e4-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="a49e4-120">Speichert alle Änderungen am Link.</span><span class="sxs-lookup"><span data-stu-id="a49e4-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="a49e4-121">**Standort Standort**</span><span class="sxs-lookup"><span data-stu-id="a49e4-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="a49e4-122">Legt den Speicherort des Symbols fest, das dem Link zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a49e4-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="a49e4-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49e4-123">Properties</span></span>

<span data-ttu-id="a49e4-124">Das **shelllinkobject** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a49e4-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="a49e4-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a49e4-125">Property</span></span>                                                                | <span data-ttu-id="a49e4-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a49e4-126">Access type</span></span>           | <span data-ttu-id="a49e4-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a49e4-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a49e4-128">**Argumente**</span><span class="sxs-lookup"><span data-stu-id="a49e4-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="a49e4-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a49e4-129">Read/write</span></span><br/> | <span data-ttu-id="a49e4-130">Enthält die Argumente eines Links.</span><span class="sxs-lookup"><span data-stu-id="a49e4-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="a49e4-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a49e4-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="a49e4-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a49e4-132">Read/write</span></span><br/> | <span data-ttu-id="a49e4-133">Ruft die Beschreibung des links ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="a49e4-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="a49e4-134">**Hotkey**</span><span class="sxs-lookup"><span data-stu-id="a49e4-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="a49e4-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a49e4-135">Read/write</span></span><br/> | <span data-ttu-id="a49e4-136">Ruft die Tastenkombination für den Link ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="a49e4-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="a49e4-137">**`Path`**</span><span class="sxs-lookup"><span data-stu-id="a49e4-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="a49e4-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a49e4-138">Read/write</span></span><br/> | <span data-ttu-id="a49e4-139">Ruft den Pfad zum Link Objekt ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="a49e4-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="a49e4-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="a49e4-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="a49e4-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a49e4-141">Read/write</span></span><br/> | <span data-ttu-id="a49e4-142">Ruft den anfänglichen Anzeige Zustand (Größen, minimiert oder maximiert) des Befehls des links ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a49e4-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="a49e4-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="a49e4-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="a49e4-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a49e4-144">Read/write</span></span><br/> | <span data-ttu-id="a49e4-145">Ruft das im Link angegebene Arbeitsverzeichnis ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="a49e4-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="a49e4-146">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a49e4-146">Requirements</span></span>



| <span data-ttu-id="a49e4-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a49e4-147">Requirement</span></span> | <span data-ttu-id="a49e4-148">Wert</span><span class="sxs-lookup"><span data-stu-id="a49e4-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49e4-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a49e4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a49e4-150">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a49e4-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a49e4-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a49e4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a49e4-152">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a49e4-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a49e4-153">Header</span><span class="sxs-lookup"><span data-stu-id="a49e4-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a49e4-154"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a49e4-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a49e4-155">IDL</span><span class="sxs-lookup"><span data-stu-id="a49e4-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a49e4-156"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a49e4-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a49e4-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a49e4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a49e4-158"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a49e4-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a49e4-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a49e4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49e4-160">Shelllinks</span><span class="sxs-lookup"><span data-stu-id="a49e4-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
