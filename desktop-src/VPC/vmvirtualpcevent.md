---
title: Vmvirtualpcevent-Enumeration (vpccominterfaces. h)
description: Gibt die Windows Virtual PC-Ereignisse an.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- Vmvirtualpcevent-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040996"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="433c1-104">Vmvirtualpcevent-Enumeration</span><span class="sxs-lookup"><span data-stu-id="433c1-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="433c1-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="433c1-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="433c1-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="433c1-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="433c1-107">Gibt die Windows Virtual PC-Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="433c1-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="433c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="433c1-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="433c1-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="433c1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="433c1-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmvirtualpcevent \_ vmstatechange**</span><span class="sxs-lookup"><span data-stu-id="433c1-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="433c1-111">Der Status einer virtuellen Maschine wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="433c1-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="433c1-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmvirtualpcevent-Ereignis \_ protokolliert**</span><span class="sxs-lookup"><span data-stu-id="433c1-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="433c1-113">Ein Ereignis wurde von Virtual PC protokolliert.</span><span class="sxs-lookup"><span data-stu-id="433c1-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="433c1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="433c1-114">Requirements</span></span>



| <span data-ttu-id="433c1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="433c1-115">Requirement</span></span> | <span data-ttu-id="433c1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="433c1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="433c1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="433c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="433c1-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="433c1-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="433c1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="433c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="433c1-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="433c1-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="433c1-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="433c1-121">End of client support</span></span><br/>    | <span data-ttu-id="433c1-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="433c1-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="433c1-123">Produkt</span><span class="sxs-lookup"><span data-stu-id="433c1-123">Product</span></span><br/>                  | <span data-ttu-id="433c1-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="433c1-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="433c1-125">Header</span><span class="sxs-lookup"><span data-stu-id="433c1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="433c1-126"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="433c1-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433c1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="433c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433c1-128">**Ivmvirtualpcevents**</span><span class="sxs-lookup"><span data-stu-id="433c1-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

