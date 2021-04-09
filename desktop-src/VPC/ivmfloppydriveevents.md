---
title: Ivmfloppydriveevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmfloppydrive-Schnittstelle. Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von ivmfloppydrive gesendet werden.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Ivmfloppydriveevents-Schnittstelle virtueller PC
- Ivmfloppydriveevents Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106059"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="52da4-106">Ivmfloppydriveevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="52da4-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="52da4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52da4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52da4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52da4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52da4-109">Definiert die ausgehende Ereignis Schnittstelle für die [**ivmfloppydrive**](ivmfloppydrive.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="52da4-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="52da4-110">Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von **ivmfloppydrive** gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="52da4-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="52da4-111">Member</span><span class="sxs-lookup"><span data-stu-id="52da4-111">Members</span></span>

<span data-ttu-id="52da4-112">Die **ivmfloppydriveevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="52da4-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="52da4-113">**Ivmfloppydriveevents** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52da4-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="52da4-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="52da4-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52da4-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="52da4-115">Methods</span></span>

<span data-ttu-id="52da4-116">Die **ivmfloppydriveevents** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52da4-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="52da4-117">Methode</span><span class="sxs-lookup"><span data-stu-id="52da4-117">Method</span></span>                                                      | <span data-ttu-id="52da4-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52da4-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="52da4-119">**Onmediaeject**</span><span class="sxs-lookup"><span data-stu-id="52da4-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="52da4-120">Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="52da4-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="52da4-121">**Onmediainsert**</span><span class="sxs-lookup"><span data-stu-id="52da4-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="52da4-122">Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="52da4-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="52da4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52da4-123">Requirements</span></span>



| <span data-ttu-id="52da4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52da4-124">Requirement</span></span> | <span data-ttu-id="52da4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="52da4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52da4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52da4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52da4-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52da4-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52da4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52da4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52da4-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52da4-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52da4-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="52da4-130">End of client support</span></span><br/>    | <span data-ttu-id="52da4-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52da4-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52da4-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="52da4-132">Product</span></span><br/>                  | <span data-ttu-id="52da4-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52da4-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52da4-134">Header</span><span class="sxs-lookup"><span data-stu-id="52da4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="52da4-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52da4-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52da4-136">IID</span><span class="sxs-lookup"><span data-stu-id="52da4-136">IID</span></span><br/>                      | <span data-ttu-id="52da4-137">Diid \_ ivmfloppydriveevents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.</span><span class="sxs-lookup"><span data-stu-id="52da4-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

