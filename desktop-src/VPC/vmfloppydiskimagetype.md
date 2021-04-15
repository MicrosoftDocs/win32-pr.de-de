---
title: Vmfloppydiskimagetype-Enumeration (vpccominterfaces. h)
description: Gibt die Disketten Formate an.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- Vmfloppydiskimagetype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391897"
---
# <a name="vmfloppydiskimagetype-enumeration"></a><span data-ttu-id="422f5-104">Vmfloppydiskimagetype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="422f5-104">VMFloppyDiskImageType enumeration</span></span>

<span data-ttu-id="422f5-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="422f5-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="422f5-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="422f5-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="422f5-107">Gibt die Disketten Formate an.</span><span class="sxs-lookup"><span data-stu-id="422f5-107">Specifies the floppy disk formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="422f5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="422f5-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a><span data-ttu-id="422f5-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="422f5-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="422f5-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmfloppydiskimage \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="422f5-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-111">Unbekanntes Format.</span><span class="sxs-lookup"><span data-stu-id="422f5-111">Unknown format.</span></span>

</dd> <dt>

<span data-ttu-id="422f5-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmfloppydiskimage- \_ lowdensity**</span><span class="sxs-lookup"><span data-stu-id="422f5-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage\_LowDensity**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-113">Ein Format mit niedriger Dichte (720K).</span><span class="sxs-lookup"><span data-stu-id="422f5-113">A low density format (720K).</span></span>

</dd> <dt>

<span data-ttu-id="422f5-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmfloppydiskimage- \_ highdensity**</span><span class="sxs-lookup"><span data-stu-id="422f5-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage\_HighDensity**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-115">Ein Format mit hoher Dichte (1,44 MB).</span><span class="sxs-lookup"><span data-stu-id="422f5-115">A high density format (1.44MB).</span></span>

</dd> <dt>

<span data-ttu-id="422f5-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmfloppydiskimage- \_ DMF**</span><span class="sxs-lookup"><span data-stu-id="422f5-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage\_DMF**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-117">Ein Verteilungs Medienformat (1,68 MB).</span><span class="sxs-lookup"><span data-stu-id="422f5-117">A distribution media format (1.68Mb).</span></span>

</dd> <dt>

<span data-ttu-id="422f5-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmfloppydiskimage \_ lowdensitysingleseitiges**</span><span class="sxs-lookup"><span data-stu-id="422f5-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage\_LowDensitySingleSided**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-119">Ein einseitiges Format mit niedriger Dichte.</span><span class="sxs-lookup"><span data-stu-id="422f5-119">A single-sided low density format.</span></span>

</dd> <dt>

<span data-ttu-id="422f5-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**"vmfloppydiskimage" \_ mediumschlag Density**</span><span class="sxs-lookup"><span data-stu-id="422f5-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage\_MediumDensity**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-121">Ein mittelgroßes Dichte Format (1,2 MB).</span><span class="sxs-lookup"><span data-stu-id="422f5-121">A medium density format (1.2MB).</span></span>

</dd> <dt>

<span data-ttu-id="422f5-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmfloppydiskimage \_ highdensitymss**</span><span class="sxs-lookup"><span data-stu-id="422f5-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage\_HighDensityMSS**</span></span>
</dt> <dd>

<span data-ttu-id="422f5-123">Eine MSS (Multiple sektorsize) mit hoher Dichte, die vom erweiterten Verteilungs Format (Xdf) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="422f5-123">A high-density Multiple Sector Size (MSS), used by eXtended Distribution Format (XDF).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="422f5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="422f5-124">Requirements</span></span>



| <span data-ttu-id="422f5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="422f5-125">Requirement</span></span> | <span data-ttu-id="422f5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="422f5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="422f5-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="422f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="422f5-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="422f5-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="422f5-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="422f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="422f5-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="422f5-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="422f5-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="422f5-131">End of client support</span></span><br/>    | <span data-ttu-id="422f5-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="422f5-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="422f5-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="422f5-133">Product</span></span><br/>                  | <span data-ttu-id="422f5-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="422f5-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="422f5-135">Header</span><span class="sxs-lookup"><span data-stu-id="422f5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="422f5-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="422f5-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422f5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="422f5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422f5-138">**Ivmvirtualpc:: kreatefloppydiskimage**</span><span class="sxs-lookup"><span data-stu-id="422f5-138">**IVMVirtualPC::CreateFloppyDiskImage**</span></span>](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[<span data-ttu-id="422f5-139">**Ivmvirtualpc:: getfloppydiskimagetype**</span><span class="sxs-lookup"><span data-stu-id="422f5-139">**IVMVirtualPC::GetFloppyDiskImageType**</span></span>](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

