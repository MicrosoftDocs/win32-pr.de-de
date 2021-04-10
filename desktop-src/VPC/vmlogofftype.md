---
title: Vmlogofftype-Enumeration (vpccominterfaces. h)
description: Gibt an, wie ein virtueller Computer heruntergefahren wird.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Vmlogofftype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040564"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="88c7c-104">Vmlogofftype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="88c7c-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="88c7c-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88c7c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88c7c-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88c7c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88c7c-107">Gibt an, wie ein virtueller Computer (VM) heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="88c7c-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="88c7c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88c7c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="88c7c-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="88c7c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88c7c-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmlogoff \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="88c7c-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="88c7c-111">Die Abmeldung auf der Gast-VM war normal.</span><span class="sxs-lookup"><span data-stu-id="88c7c-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="88c7c-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmlogoff \_ erzwungen**</span><span class="sxs-lookup"><span data-stu-id="88c7c-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="88c7c-113">Die Abmeldung in der Gast-VM wurde erzwungen.</span><span class="sxs-lookup"><span data-stu-id="88c7c-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="88c7c-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmlogoff \_ extern**</span><span class="sxs-lookup"><span data-stu-id="88c7c-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="88c7c-115">Die Abmeldung auf der Gast-VM wurde mithilfe der [**ivmguestos:: Abmeldung**](ivmguestos-logoff.md) -Methode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88c7c-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88c7c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88c7c-116">Requirements</span></span>



| <span data-ttu-id="88c7c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88c7c-117">Requirement</span></span> | <span data-ttu-id="88c7c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="88c7c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c7c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88c7c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88c7c-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88c7c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88c7c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88c7c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88c7c-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88c7c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88c7c-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="88c7c-123">End of client support</span></span><br/>    | <span data-ttu-id="88c7c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88c7c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88c7c-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="88c7c-125">Product</span></span><br/>                  | <span data-ttu-id="88c7c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88c7c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88c7c-127">Header</span><span class="sxs-lookup"><span data-stu-id="88c7c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c7c-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c7c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c7c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88c7c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c7c-130">**Ivmvirtualmachine:: shutdownaktiononquit**</span><span class="sxs-lookup"><span data-stu-id="88c7c-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

