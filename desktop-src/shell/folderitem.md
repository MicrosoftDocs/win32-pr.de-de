---
description: Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.
title: FolderItem-Objekt (Shldisp. h)
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
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484027"
---
# <a name="folderitem-object"></a><span data-ttu-id="7eae6-104">FolderItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="7eae6-104">FolderItem object</span></span>

<span data-ttu-id="7eae6-105">Stellt ein Element in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="7eae6-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="7eae6-106">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.</span><span class="sxs-lookup"><span data-stu-id="7eae6-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="7eae6-107">Member</span><span class="sxs-lookup"><span data-stu-id="7eae6-107">Members</span></span>

<span data-ttu-id="7eae6-108">Das **folderItem** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7eae6-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="7eae6-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="7eae6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7eae6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7eae6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7eae6-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7eae6-111">Methods</span></span>

<span data-ttu-id="7eae6-112">Das **folderItem** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7eae6-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="7eae6-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7eae6-113">Method</span></span>                                      | <span data-ttu-id="7eae6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7eae6-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7eae6-115">**Invokeverb**</span><span class="sxs-lookup"><span data-stu-id="7eae6-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="7eae6-116">Führt ein Verb für das Element aus.</span><span class="sxs-lookup"><span data-stu-id="7eae6-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="7eae6-117">**Verben**</span><span class="sxs-lookup"><span data-stu-id="7eae6-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="7eae6-118">Ruft das [**folderitemverbs**](folderitemverbs.md) -Objekt des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="7eae6-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="7eae6-119">Bei diesem Objekt handelt es sich um eine Auflistung von Verben, die für das Element ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="7eae6-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7eae6-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7eae6-120">Properties</span></span>

<span data-ttu-id="7eae6-121">Das **folderItem** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7eae6-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="7eae6-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7eae6-122">Property</span></span>                                                   | <span data-ttu-id="7eae6-123">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7eae6-123">Access type</span></span>           | <span data-ttu-id="7eae6-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7eae6-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7eae6-125">**Application**</span><span class="sxs-lookup"><span data-stu-id="7eae6-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="7eae6-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-126">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-127">Enthält das [**Anwendungs**](folderitem-application.md) Objekt des Ordner Elements.</span><span class="sxs-lookup"><span data-stu-id="7eae6-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="7eae6-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="7eae6-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="7eae6-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-129">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-130">Enthält das [**Ordner**](folder.md) Objekt des Elements, wenn es sich bei dem Element um einen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="7eae6-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="7eae6-131">**Getlink**</span><span class="sxs-lookup"><span data-stu-id="7eae6-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="7eae6-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-132">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-133">Enthält das [**shelllinkobject**](shelllinkobject-object.md) -Objekt des Elements, wenn das Element eine Verknüpfung ist.</span><span class="sxs-lookup"><span data-stu-id="7eae6-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="7eae6-134">**Isbrowsefähig**</span><span class="sxs-lookup"><span data-stu-id="7eae6-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="7eae6-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-135">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-136">Gibt an, ob das Element in einem Browser-oder Windows-Explorer-Frame gehostet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7eae6-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="7eae6-137">**IsFile System**</span><span class="sxs-lookup"><span data-stu-id="7eae6-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="7eae6-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-138">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-139">Gibt an, ob das Element Teil des Dateisystems ist.</span><span class="sxs-lookup"><span data-stu-id="7eae6-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="7eae6-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="7eae6-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="7eae6-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-141">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-142">Gibt an, ob das Element ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="7eae6-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="7eae6-143">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="7eae6-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="7eae6-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-144">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-145">Gibt an, ob das Element eine Verknüpfung ist.</span><span class="sxs-lookup"><span data-stu-id="7eae6-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="7eae6-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="7eae6-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="7eae6-147">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7eae6-147">Read/write</span></span><br/> | <span data-ttu-id="7eae6-148">Ruft das Datum und die Uhrzeit der letzten Änderung einer Datei ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7eae6-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="7eae6-149">Mit " [**ModifyDate**](folderitem-modifydate.md) " können das Datum und die Uhrzeit der letzten Änderung eines Ordners abgerufen, jedoch nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7eae6-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="7eae6-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="7eae6-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="7eae6-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7eae6-151">Read/write</span></span><br/> | <span data-ttu-id="7eae6-152">Legt den Namen des Elements fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="7eae6-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="7eae6-153">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7eae6-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="7eae6-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-154">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-155">Ruft ein-Objekt ab, das das übergeordnete Element des Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="7eae6-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="7eae6-156">**`Path`**</span><span class="sxs-lookup"><span data-stu-id="7eae6-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="7eae6-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-157">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-158">Enthält den vollständigen Pfad und den Namen des Elements.</span><span class="sxs-lookup"><span data-stu-id="7eae6-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="7eae6-159">**Size**</span><span class="sxs-lookup"><span data-stu-id="7eae6-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="7eae6-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-160">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-161">Enthält die Größe des Elements.</span><span class="sxs-lookup"><span data-stu-id="7eae6-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="7eae6-162">**Sorte**</span><span class="sxs-lookup"><span data-stu-id="7eae6-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="7eae6-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eae6-163">Read-only</span></span><br/>  | <span data-ttu-id="7eae6-164">Enthält eine Zeichen folgen Darstellung des Elementtyps.</span><span class="sxs-lookup"><span data-stu-id="7eae6-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="7eae6-165">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7eae6-165">Requirements</span></span>



| <span data-ttu-id="7eae6-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7eae6-166">Requirement</span></span> | <span data-ttu-id="7eae6-167">Wert</span><span class="sxs-lookup"><span data-stu-id="7eae6-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eae6-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7eae6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7eae6-169">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7eae6-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7eae6-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7eae6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7eae6-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7eae6-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7eae6-172">Header</span><span class="sxs-lookup"><span data-stu-id="7eae6-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eae6-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7eae6-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7eae6-174">IDL</span><span class="sxs-lookup"><span data-stu-id="7eae6-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7eae6-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7eae6-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7eae6-176">DLL</span><span class="sxs-lookup"><span data-stu-id="7eae6-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eae6-177"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7eae6-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




