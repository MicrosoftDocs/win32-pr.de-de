---
description: Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.
title: FolderItem-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840981"
---
# <a name="folderitem-object"></a><span data-ttu-id="41b4c-104">FolderItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="41b4c-104">FolderItem object</span></span>

<span data-ttu-id="41b4c-105">Stellt ein Element in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="41b4c-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="41b4c-106">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Element abrufen können.</span><span class="sxs-lookup"><span data-stu-id="41b4c-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="41b4c-107">Member</span><span class="sxs-lookup"><span data-stu-id="41b4c-107">Members</span></span>

<span data-ttu-id="41b4c-108">Das **FolderItem-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="41b4c-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="41b4c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="41b4c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="41b4c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41b4c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41b4c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="41b4c-111">Methods</span></span>

<span data-ttu-id="41b4c-112">Das **FolderItem-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="41b4c-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="41b4c-113">Methode</span><span class="sxs-lookup"><span data-stu-id="41b4c-113">Method</span></span>                                      | <span data-ttu-id="41b4c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41b4c-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41b4c-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="41b4c-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="41b4c-116">Führt ein Verb für das Element aus.</span><span class="sxs-lookup"><span data-stu-id="41b4c-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="41b4c-117">**Verben**</span><span class="sxs-lookup"><span data-stu-id="41b4c-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="41b4c-118">Ruft das [**FolderItemVerbs-Objekt**](folderitemverbs.md) des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="41b4c-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="41b4c-119">Dieses Objekt ist die Auflistung von Verben, die für das Element ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="41b4c-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41b4c-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41b4c-120">Properties</span></span>

<span data-ttu-id="41b4c-121">Das **FolderItem-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41b4c-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="41b4c-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41b4c-122">Property</span></span>                                                   | <span data-ttu-id="41b4c-123">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="41b4c-123">Access type</span></span>           | <span data-ttu-id="41b4c-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41b4c-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41b4c-125">**Application**</span><span class="sxs-lookup"><span data-stu-id="41b4c-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="41b4c-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-126">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-127">Enthält das [**Application-Objekt**](folderitem-application.md) des Ordnerelements.</span><span class="sxs-lookup"><span data-stu-id="41b4c-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="41b4c-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="41b4c-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="41b4c-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-129">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-130">Enthält das [**Folder-Objekt**](folder.md) des Elements, wenn das Element ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="41b4c-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="41b4c-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="41b4c-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="41b4c-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-132">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-133">Enthält das [**ShellLinkObject-Objekt**](shelllinkobject-object.md) des Elements, wenn das Element eine Verknüpfung ist.</span><span class="sxs-lookup"><span data-stu-id="41b4c-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="41b4c-134">**IsBrowsable**</span><span class="sxs-lookup"><span data-stu-id="41b4c-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="41b4c-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-135">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-136">Gibt an, ob das Element in einem Browser oder in einem Windows-Explorer werden kann.</span><span class="sxs-lookup"><span data-stu-id="41b4c-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="41b4c-137">**IsFileSystem**</span><span class="sxs-lookup"><span data-stu-id="41b4c-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="41b4c-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-138">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-139">Gibt an, ob das Element Teil des Dateisystems ist.</span><span class="sxs-lookup"><span data-stu-id="41b4c-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="41b4c-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="41b4c-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="41b4c-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-141">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-142">Gibt an, ob das Element ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="41b4c-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="41b4c-143">**Islink**</span><span class="sxs-lookup"><span data-stu-id="41b4c-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="41b4c-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-144">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-145">Gibt an, ob das Element eine Verknüpfung ist.</span><span class="sxs-lookup"><span data-stu-id="41b4c-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="41b4c-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="41b4c-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="41b4c-147">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41b4c-147">Read/write</span></span><br/> | <span data-ttu-id="41b4c-148">Legt das Datum und die Uhrzeit der letzten Änderung einer Datei fest oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="41b4c-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="41b4c-149">[**ModifyDate kann**](folderitem-modifydate.md) verwendet werden, um das Datum und die Uhrzeit der letzten Änderung eines Ordners abzurufen, kann aber nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="41b4c-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="41b4c-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="41b4c-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="41b4c-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41b4c-151">Read/write</span></span><br/> | <span data-ttu-id="41b4c-152">Legt den Namen des Elements fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="41b4c-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="41b4c-153">**Parent**</span><span class="sxs-lookup"><span data-stu-id="41b4c-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="41b4c-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-154">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-155">Ruft ein -Objekt ab, das das übergeordnete Element des Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="41b4c-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="41b4c-156">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="41b4c-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="41b4c-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-157">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-158">Enthält den vollständigen Pfad und Namen des Elements.</span><span class="sxs-lookup"><span data-stu-id="41b4c-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="41b4c-159">**Size**</span><span class="sxs-lookup"><span data-stu-id="41b4c-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="41b4c-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-160">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-161">Enthält die Größe des Elements.</span><span class="sxs-lookup"><span data-stu-id="41b4c-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="41b4c-162">**type**</span><span class="sxs-lookup"><span data-stu-id="41b4c-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="41b4c-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41b4c-163">Read-only</span></span><br/>  | <span data-ttu-id="41b4c-164">Enthält eine Zeichenfolgendarstellung des Elementtyps.</span><span class="sxs-lookup"><span data-stu-id="41b4c-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="41b4c-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41b4c-165">Requirements</span></span>



| <span data-ttu-id="41b4c-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41b4c-166">Requirement</span></span> | <span data-ttu-id="41b4c-167">Wert</span><span class="sxs-lookup"><span data-stu-id="41b4c-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b4c-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41b4c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="41b4c-169">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41b4c-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="41b4c-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41b4c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="41b4c-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41b4c-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41b4c-172">Header</span><span class="sxs-lookup"><span data-stu-id="41b4c-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b4c-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="41b4c-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="41b4c-174">Idl</span><span class="sxs-lookup"><span data-stu-id="41b4c-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41b4c-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="41b4c-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="41b4c-176">DLL</span><span class="sxs-lookup"><span data-stu-id="41b4c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b4c-177"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="41b4c-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




