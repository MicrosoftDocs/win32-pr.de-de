---
description: Erweitert das Folder-Objekt zur Unterstützung von Offlineordnern.
title: Folder2-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842061"
---
# <a name="folder2-object"></a><span data-ttu-id="be06d-103">Folder2-Objekt</span><span class="sxs-lookup"><span data-stu-id="be06d-103">Folder2 object</span></span>

<span data-ttu-id="be06d-104">Erweitert das [**Folder-Objekt**](folder.md) zur Unterstützung von Offlineordnern.</span><span class="sxs-lookup"><span data-stu-id="be06d-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="be06d-105">Member</span><span class="sxs-lookup"><span data-stu-id="be06d-105">Members</span></span>

<span data-ttu-id="be06d-106">Das **Folder2-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="be06d-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="be06d-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="be06d-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="be06d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be06d-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be06d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="be06d-109">Methods</span></span>

<span data-ttu-id="be06d-110">Das **Folder2-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="be06d-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="be06d-111">Methode</span><span class="sxs-lookup"><span data-stu-id="be06d-111">Method</span></span>                                                                 | <span data-ttu-id="be06d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be06d-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="be06d-113">**DismissedWebViewBar llcde**</span><span class="sxs-lookup"><span data-stu-id="be06d-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="be06d-114">Wird als Reaktion darauf aufgerufen, dass die Webansichtsleiste vom Benutzer verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="be06d-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="be06d-115">**Synchronisieren**</span><span class="sxs-lookup"><span data-stu-id="be06d-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="be06d-116">Synchronisiert alle Offlinedateien im Ordner.</span><span class="sxs-lookup"><span data-stu-id="be06d-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="be06d-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be06d-117">Properties</span></span>

<span data-ttu-id="be06d-118">Das **Folder2-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be06d-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="be06d-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be06d-119">Property</span></span>                                                                            | <span data-ttu-id="be06d-120">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="be06d-120">Access type</span></span>          | <span data-ttu-id="be06d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be06d-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="be06d-122">**HaveToShowWebViewBar llcde**</span><span class="sxs-lookup"><span data-stu-id="be06d-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="be06d-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="be06d-123">Read-only</span></span><br/> | <span data-ttu-id="be06d-124">Wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be06d-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="be06d-125">**OfflineStatus**</span><span class="sxs-lookup"><span data-stu-id="be06d-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="be06d-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="be06d-126">Read-only</span></span><br/> | <span data-ttu-id="be06d-127">Enthält den Offlinestatus des Ordners.</span><span class="sxs-lookup"><span data-stu-id="be06d-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="be06d-128">**Selbst**</span><span class="sxs-lookup"><span data-stu-id="be06d-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="be06d-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="be06d-129">Read-only</span></span><br/> | <span data-ttu-id="be06d-130">Enthält das [**FolderItem-Objekt**](folderitem.md) des Ordners.</span><span class="sxs-lookup"><span data-stu-id="be06d-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be06d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be06d-131">Requirements</span></span>



| <span data-ttu-id="be06d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be06d-132">Requirement</span></span> | <span data-ttu-id="be06d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="be06d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be06d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be06d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="be06d-135">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be06d-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be06d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be06d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="be06d-137">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be06d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="be06d-138">Header</span><span class="sxs-lookup"><span data-stu-id="be06d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="be06d-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="be06d-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="be06d-140">Idl</span><span class="sxs-lookup"><span data-stu-id="be06d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be06d-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="be06d-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="be06d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="be06d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be06d-143"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="be06d-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be06d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be06d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be06d-145">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="be06d-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




