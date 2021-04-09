---
title: Vmdrivetype-Enumeration (vpccominterfaces. h)
description: Gibt den Typ des Laufwerks an, das einem Busstandort zugeordnet ist.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- Vmdrivetype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741400"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="4669f-104">Vmdrivetype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4669f-104">VMDriveType enumeration</span></span>

<span data-ttu-id="4669f-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4669f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4669f-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4669f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4669f-107">Gibt den Typ des Laufwerks an, das einem Busstandort zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4669f-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="4669f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4669f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="4669f-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4669f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4669f-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmdrivetype \_ null**</span><span class="sxs-lookup"><span data-stu-id="4669f-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="4669f-111">Es ist kein Laufwerk angefügt.</span><span class="sxs-lookup"><span data-stu-id="4669f-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="4669f-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmdrivetype- \_ Harddisk**</span><span class="sxs-lookup"><span data-stu-id="4669f-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="4669f-113">Es ist eine Festplatte angefügt.</span><span class="sxs-lookup"><span data-stu-id="4669f-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="4669f-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmdrivetype- \_ DVD**</span><span class="sxs-lookup"><span data-stu-id="4669f-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="4669f-115">Es ist ein CD-oder DVD-Laufwerk angefügt.</span><span class="sxs-lookup"><span data-stu-id="4669f-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4669f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4669f-116">Requirements</span></span>



| <span data-ttu-id="4669f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4669f-117">Requirement</span></span> | <span data-ttu-id="4669f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4669f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4669f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4669f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4669f-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4669f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4669f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4669f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4669f-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4669f-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4669f-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4669f-123">End of client support</span></span><br/>    | <span data-ttu-id="4669f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4669f-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4669f-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="4669f-125">Product</span></span><br/>                  | <span data-ttu-id="4669f-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4669f-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4669f-127">Header</span><span class="sxs-lookup"><span data-stu-id="4669f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4669f-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4669f-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4669f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4669f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4669f-130">**Ivmvirtualmachine:: attacheddrivetypes**</span><span class="sxs-lookup"><span data-stu-id="4669f-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

