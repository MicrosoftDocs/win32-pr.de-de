---
title: vmfloppydriveevent-Enumeration (vpccominterfaces. h)
description: Gibt die Disketten Laufwerks Ereignisse an.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- virtueller PC der vmfloppydriveevent-Enumeration
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743080"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="fd151-104">vmfloppydriveevent-Enumeration</span><span class="sxs-lookup"><span data-stu-id="fd151-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="fd151-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fd151-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd151-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd151-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd151-107">Gibt die Disketten Laufwerks Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="fd151-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd151-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd151-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="fd151-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="fd151-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd151-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmfloppydriveevent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="fd151-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="fd151-111">Ein Disketten Image ist angefügt oder echte Medien werden in ein Host Laufwerk eingefügt.</span><span class="sxs-lookup"><span data-stu-id="fd151-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="fd151-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmfloppydriveevent \_ oneject**</span><span class="sxs-lookup"><span data-stu-id="fd151-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="fd151-113">Medien wurden aussteht.</span><span class="sxs-lookup"><span data-stu-id="fd151-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd151-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd151-114">Requirements</span></span>



| <span data-ttu-id="fd151-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd151-115">Requirement</span></span> | <span data-ttu-id="fd151-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fd151-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd151-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd151-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd151-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd151-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd151-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd151-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd151-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd151-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd151-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fd151-121">End of client support</span></span><br/>    | <span data-ttu-id="fd151-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd151-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd151-123">Produkt</span><span class="sxs-lookup"><span data-stu-id="fd151-123">Product</span></span><br/>                  | <span data-ttu-id="fd151-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd151-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd151-125">Header</span><span class="sxs-lookup"><span data-stu-id="fd151-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd151-126"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd151-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd151-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd151-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd151-128">**Ivmfloppydriveevents**</span><span class="sxs-lookup"><span data-stu-id="fd151-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

