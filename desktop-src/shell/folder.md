---
description: Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Folder-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524491"
---
# <a name="folder-object"></a><span data-ttu-id="0fac8-104">Folder-Objekt</span><span class="sxs-lookup"><span data-stu-id="0fac8-104">Folder object</span></span>

<span data-ttu-id="0fac8-105">Stellt einen Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="0fac8-105">Represents a Shell folder.</span></span> <span data-ttu-id="0fac8-106">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.</span><span class="sxs-lookup"><span data-stu-id="0fac8-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="0fac8-107">Member</span><span class="sxs-lookup"><span data-stu-id="0fac8-107">Members</span></span>

<span data-ttu-id="0fac8-108">Das **Ordner** Objekt enthält die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0fac8-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="0fac8-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0fac8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0fac8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fac8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0fac8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0fac8-111">Methods</span></span>

<span data-ttu-id="0fac8-112">Das **Folder** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0fac8-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="0fac8-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0fac8-113">Method</span></span>                                      | <span data-ttu-id="0fac8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fac8-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fac8-115">**Copyhere**</span><span class="sxs-lookup"><span data-stu-id="0fac8-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="0fac8-116">Kopiert ein Element oder Elemente in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0fac8-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="0fac8-117">**GetDetailsOf**</span><span class="sxs-lookup"><span data-stu-id="0fac8-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="0fac8-118">Ruft Details zu einem Element in einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="0fac8-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="0fac8-119">Beispielsweise Größe, Typ oder Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="0fac8-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="0fac8-120">**Items**</span><span class="sxs-lookup"><span data-stu-id="0fac8-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="0fac8-121">Ruft ein [**folderitems**](folderitems.md) -Objekt ab, das die Auflistung der Elemente im Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fac8-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="0fac8-122">**Muvehere**</span><span class="sxs-lookup"><span data-stu-id="0fac8-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="0fac8-123">Verschiebt ein Element oder Elemente in diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0fac8-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="0fac8-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="0fac8-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="0fac8-125">Erstellt einen neuen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0fac8-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0fac8-126">**PARSENAME**</span><span class="sxs-lookup"><span data-stu-id="0fac8-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="0fac8-127">Erstellt ein [**folderItem**](folderitem.md) -Objekt, das ein bestimmtes Element darstellt, und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="0fac8-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="0fac8-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fac8-128">Properties</span></span>

<span data-ttu-id="0fac8-129">Das **Ordner** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fac8-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="0fac8-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0fac8-130">Property</span></span>                                               | <span data-ttu-id="0fac8-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="0fac8-131">Access type</span></span>          | <span data-ttu-id="0fac8-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fac8-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="0fac8-133">**Application**</span><span class="sxs-lookup"><span data-stu-id="0fac8-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="0fac8-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fac8-134">Read-only</span></span><br/> | <span data-ttu-id="0fac8-135">Enthält das Anwendungs Objekt des Ordners.</span><span class="sxs-lookup"><span data-stu-id="0fac8-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="0fac8-136">**Parent**</span><span class="sxs-lookup"><span data-stu-id="0fac8-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="0fac8-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fac8-137">Read-only</span></span><br/> | <span data-ttu-id="0fac8-138">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0fac8-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="0fac8-139">**Ordner "Ordner"**</span><span class="sxs-lookup"><span data-stu-id="0fac8-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="0fac8-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fac8-140">Read-only</span></span><br/> | <span data-ttu-id="0fac8-141">Enthält das übergeordnete **Ordner** Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fac8-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="0fac8-142">**Titel**</span><span class="sxs-lookup"><span data-stu-id="0fac8-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="0fac8-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fac8-143">Read-only</span></span><br/> | <span data-ttu-id="0fac8-144">Enthält den Titel des Ordners.</span><span class="sxs-lookup"><span data-stu-id="0fac8-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="0fac8-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fac8-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0fac8-146">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="0fac8-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="0fac8-147">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="0fac8-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="0fac8-148">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0fac8-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fac8-149">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0fac8-149">Requirements</span></span>



| <span data-ttu-id="0fac8-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fac8-150">Requirement</span></span> | <span data-ttu-id="0fac8-151">Wert</span><span class="sxs-lookup"><span data-stu-id="0fac8-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fac8-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fac8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0fac8-153">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fac8-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="0fac8-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fac8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0fac8-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fac8-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0fac8-156">Header</span><span class="sxs-lookup"><span data-stu-id="0fac8-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fac8-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fac8-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fac8-158">IDL</span><span class="sxs-lookup"><span data-stu-id="0fac8-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fac8-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fac8-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




