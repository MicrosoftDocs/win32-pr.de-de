---
title: Vmdvddriveevent-Enumeration (vpccominterfaces. h)
description: Gibt die DVD-Laufwerks Ereignisse an.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Virtueller PC der vmdvddriveevent-Enumeration
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741393"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="a0b2c-104">Vmdvddriveevent-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a0b2c-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="a0b2c-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0b2c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a0b2c-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a0b2c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a0b2c-107">Gibt die DVD-Laufwerks Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="a0b2c-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b2c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b2c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="a0b2c-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a0b2c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a0b2c-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmdvddriveevent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="a0b2c-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="a0b2c-111">Ein ISO-Abbild ist angefügt oder echte Medien werden in ein Host Laufwerk eingefügt.</span><span class="sxs-lookup"><span data-stu-id="a0b2c-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="a0b2c-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmdvddriveevent \_ oneject**</span><span class="sxs-lookup"><span data-stu-id="a0b2c-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="a0b2c-113">Das Medium wurde ausgestoßen.</span><span class="sxs-lookup"><span data-stu-id="a0b2c-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0b2c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0b2c-114">Requirements</span></span>



| <span data-ttu-id="a0b2c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0b2c-115">Requirement</span></span> | <span data-ttu-id="a0b2c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a0b2c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b2c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0b2c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b2c-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0b2c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0b2c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0b2c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b2c-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a0b2c-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a0b2c-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a0b2c-121">End of client support</span></span><br/>    | <span data-ttu-id="a0b2c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0b2c-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a0b2c-123">Produkt</span><span class="sxs-lookup"><span data-stu-id="a0b2c-123">Product</span></span><br/>                  | <span data-ttu-id="a0b2c-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a0b2c-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a0b2c-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0b2c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b2c-126"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b2c-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b2c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0b2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b2c-128">**Ivmdvddriveevents**</span><span class="sxs-lookup"><span data-stu-id="a0b2c-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

