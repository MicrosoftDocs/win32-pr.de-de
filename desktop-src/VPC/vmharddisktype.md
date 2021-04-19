---
title: Vmharddisktype-Enumeration (vpccominterfaces. h)
description: Gibt den Bildtyp der Festplatte an.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- Virtueller PC der vmharddisktype-Enumeration
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342458"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="ddf61-104">Vmharddisktype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ddf61-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="ddf61-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ddf61-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ddf61-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ddf61-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ddf61-107">Gibt den Bildtyp der Festplatte an.</span><span class="sxs-lookup"><span data-stu-id="ddf61-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf61-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddf61-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="ddf61-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ddf61-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ddf61-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmdisktype \_ Dynamic**</span><span class="sxs-lookup"><span data-stu-id="ddf61-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="ddf61-111">Ein dynamisch erweiterendes Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="ddf61-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="ddf61-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmdisktype \_ FixedSize**</span><span class="sxs-lookup"><span data-stu-id="ddf61-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="ddf61-113">Ein Festplatten Abbild mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="ddf61-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="ddf61-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**"vmdisktype"- \_ Differenzierung**</span><span class="sxs-lookup"><span data-stu-id="ddf61-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="ddf61-115">Ein differenzierender Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="ddf61-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddf61-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddf61-116">Requirements</span></span>



| <span data-ttu-id="ddf61-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddf61-117">Requirement</span></span> | <span data-ttu-id="ddf61-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ddf61-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf61-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddf61-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ddf61-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddf61-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ddf61-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddf61-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ddf61-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ddf61-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ddf61-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ddf61-123">End of client support</span></span><br/>    | <span data-ttu-id="ddf61-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ddf61-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ddf61-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="ddf61-125">Product</span></span><br/>                  | <span data-ttu-id="ddf61-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ddf61-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ddf61-127">Header</span><span class="sxs-lookup"><span data-stu-id="ddf61-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddf61-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf61-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf61-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddf61-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf61-130">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="ddf61-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

