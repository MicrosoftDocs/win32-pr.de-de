---
title: Imsrdpdrivecollection-Schnittstelle
description: Stellt eine Auflistung von Laufwerk Objekten dar.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477736"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="dc588-105">Imsrdpdrivecollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dc588-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="dc588-106">Stellt eine Auflistung von Laufwerk Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="dc588-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="dc588-107">Member</span><span class="sxs-lookup"><span data-stu-id="dc588-107">Members</span></span>

<span data-ttu-id="dc588-108">Die **imsrdpdrivecollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dc588-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc588-109">**Imsrdpdrivecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc588-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="dc588-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="dc588-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc588-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc588-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc588-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="dc588-112">Methods</span></span>

<span data-ttu-id="dc588-113">Die **imsrdpdrivecollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dc588-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="dc588-114">Methode</span><span class="sxs-lookup"><span data-stu-id="dc588-114">Method</span></span>                                                     | <span data-ttu-id="dc588-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc588-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="dc588-116">**Neu eingängig**</span><span class="sxs-lookup"><span data-stu-id="dc588-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="dc588-117">Aktualisiert die Liste der-Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="dc588-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc588-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc588-118">Properties</span></span>

<span data-ttu-id="dc588-119">Die **imsrdpdrivecollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc588-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="dc588-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc588-120">Property</span></span>                                                              | <span data-ttu-id="dc588-121">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="dc588-121">Access type</span></span>          | <span data-ttu-id="dc588-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc588-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="dc588-123">**Drivebyindex**</span><span class="sxs-lookup"><span data-stu-id="dc588-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="dc588-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc588-124">Read-only</span></span><br/> | <span data-ttu-id="dc588-125">Ruft das Laufwerk am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="dc588-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="dc588-126">**Drivecount**</span><span class="sxs-lookup"><span data-stu-id="dc588-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="dc588-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc588-127">Read-only</span></span><br/> | <span data-ttu-id="dc588-128">Ruft die Anzahl der-Objekte in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="dc588-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc588-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc588-129">Requirements</span></span>



| <span data-ttu-id="dc588-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc588-130">Requirement</span></span> | <span data-ttu-id="dc588-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dc588-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc588-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc588-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dc588-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc588-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="dc588-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc588-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dc588-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc588-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="dc588-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dc588-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc588-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc588-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="dc588-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dc588-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc588-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc588-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="dc588-140">IID</span><span class="sxs-lookup"><span data-stu-id="dc588-140">IID</span></span><br/>                      | <span data-ttu-id="dc588-141">IID \_ imsrdpdrivecollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.</span><span class="sxs-lookup"><span data-stu-id="dc588-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc588-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc588-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc588-143">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="dc588-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="dc588-144">**Imsrdpdrive**</span><span class="sxs-lookup"><span data-stu-id="dc588-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

