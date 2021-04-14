---
title: Ivmdvddriveevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmdvddrive-Schnittstelle.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Ivmdvddriveevents-Schnittstelle virtueller PC
- Virtueller Computer für ivmdvddriveevents Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479011"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="b0e6e-105">Ivmdvddriveevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b0e6e-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="b0e6e-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b0e6e-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b0e6e-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b0e6e-108">Definiert die ausgehende Ereignis Schnittstelle für die [**ivmdvddrive**](ivmdvddrive.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="b0e6e-109">Member</span><span class="sxs-lookup"><span data-stu-id="b0e6e-109">Members</span></span>

<span data-ttu-id="b0e6e-110">Die **ivmdvddriveevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b0e6e-111">**Ivmdvddriveevents** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b0e6e-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="b0e6e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b0e6e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b0e6e-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b0e6e-113">Methods</span></span>

<span data-ttu-id="b0e6e-114">Die **ivmdvddriveevents** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="b0e6e-115">Methode</span><span class="sxs-lookup"><span data-stu-id="b0e6e-115">Method</span></span>                                                   | <span data-ttu-id="b0e6e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0e6e-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="b0e6e-117">**Onmediaeject**</span><span class="sxs-lookup"><span data-stu-id="b0e6e-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="b0e6e-118">Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="b0e6e-119">**Onmediainsert**</span><span class="sxs-lookup"><span data-stu-id="b0e6e-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="b0e6e-120">Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0e6e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0e6e-121">Requirements</span></span>



| <span data-ttu-id="b0e6e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0e6e-122">Requirement</span></span> | <span data-ttu-id="b0e6e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b0e6e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e6e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0e6e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e6e-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e6e-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0e6e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0e6e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e6e-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b0e6e-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b0e6e-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b0e6e-128">End of client support</span></span><br/>    | <span data-ttu-id="b0e6e-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0e6e-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b0e6e-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="b0e6e-130">Product</span></span><br/>                  | <span data-ttu-id="b0e6e-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b0e6e-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b0e6e-132">Header</span><span class="sxs-lookup"><span data-stu-id="b0e6e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e6e-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e6e-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b0e6e-134">IID</span><span class="sxs-lookup"><span data-stu-id="b0e6e-134">IID</span></span><br/>                      | <span data-ttu-id="b0e6e-135">Diid \_ ivmdvddriveevents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

