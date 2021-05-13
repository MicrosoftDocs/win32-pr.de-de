---
description: Verwaltet Shelllinks. Dieses Objekt macht einen Großteil der Funktionalität der IShellLink-Schnittstelle für Skriptanwendungen verfügbar.
title: ShellLinkObject-Objekt (Shldisp.h)
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
ms.openlocfilehash: 5862ae3c9b7bf1262edbc28b06f2963f2e577275
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842631"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="6521e-104">ShellLinkObject-Objekt</span><span class="sxs-lookup"><span data-stu-id="6521e-104">ShellLinkObject object</span></span>

<span data-ttu-id="6521e-105">Verwaltet Shelllinks.</span><span class="sxs-lookup"><span data-stu-id="6521e-105">Manages Shell links.</span></span> <span data-ttu-id="6521e-106">Dieses Objekt macht einen Großteil der Funktionalität der [**IShellLink-Schnittstelle**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) für Skriptanwendungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6521e-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="6521e-107">Member</span><span class="sxs-lookup"><span data-stu-id="6521e-107">Members</span></span>

<span data-ttu-id="6521e-108">Das **ShellLinkObject-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6521e-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="6521e-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="6521e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6521e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6521e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6521e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6521e-111">Methods</span></span>

<span data-ttu-id="6521e-112">Das **ShellLinkObject-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6521e-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="6521e-113">Methode</span><span class="sxs-lookup"><span data-stu-id="6521e-113">Method</span></span>                                                     | <span data-ttu-id="6521e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6521e-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6521e-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="6521e-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="6521e-116">Ruft die Position des Symbols ab, das dem Link zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6521e-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="6521e-117">**Beheben**</span><span class="sxs-lookup"><span data-stu-id="6521e-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="6521e-118">Sucht nach dem Ziel eines Shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="6521e-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="6521e-119">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="6521e-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="6521e-120">Speichert alle Änderungen am Link.</span><span class="sxs-lookup"><span data-stu-id="6521e-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="6521e-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="6521e-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="6521e-122">Legt die Position des Symbols fest, das dem Link zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6521e-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="6521e-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6521e-123">Properties</span></span>

<span data-ttu-id="6521e-124">Das **ShellLinkObject-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6521e-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="6521e-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6521e-125">Property</span></span>                                                                | <span data-ttu-id="6521e-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="6521e-126">Access type</span></span>           | <span data-ttu-id="6521e-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6521e-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6521e-128">**Argumente**</span><span class="sxs-lookup"><span data-stu-id="6521e-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="6521e-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6521e-129">Read/write</span></span><br/> | <span data-ttu-id="6521e-130">Enthält die Argumente eines Links.</span><span class="sxs-lookup"><span data-stu-id="6521e-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="6521e-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6521e-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="6521e-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6521e-132">Read/write</span></span><br/> | <span data-ttu-id="6521e-133">Ruft die Beschreibung des Links ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6521e-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="6521e-134">**Hotkey**</span><span class="sxs-lookup"><span data-stu-id="6521e-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="6521e-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6521e-135">Read/write</span></span><br/> | <span data-ttu-id="6521e-136">Ruft die Tastenkombination für den Link ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6521e-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="6521e-137">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="6521e-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="6521e-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6521e-138">Read/write</span></span><br/> | <span data-ttu-id="6521e-139">Ruft den Pfad zum Linkobjekt ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="6521e-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="6521e-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="6521e-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="6521e-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6521e-141">Read/write</span></span><br/> | <span data-ttu-id="6521e-142">Ruft den anfänglichen Anzeigezustand (größe, minimiert oder maximiert) des Linkbefehls ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="6521e-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="6521e-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="6521e-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="6521e-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6521e-144">Read/write</span></span><br/> | <span data-ttu-id="6521e-145">Ruft das im Link angegebene Arbeitsverzeichnis ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="6521e-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="6521e-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6521e-146">Requirements</span></span>



| <span data-ttu-id="6521e-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6521e-147">Requirement</span></span> | <span data-ttu-id="6521e-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6521e-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6521e-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6521e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6521e-150">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6521e-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6521e-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6521e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6521e-152">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6521e-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6521e-153">Header</span><span class="sxs-lookup"><span data-stu-id="6521e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6521e-154"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6521e-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6521e-155">Idl</span><span class="sxs-lookup"><span data-stu-id="6521e-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6521e-156"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6521e-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6521e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6521e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6521e-158"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6521e-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6521e-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6521e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6521e-160">Shelllinks</span><span class="sxs-lookup"><span data-stu-id="6521e-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
