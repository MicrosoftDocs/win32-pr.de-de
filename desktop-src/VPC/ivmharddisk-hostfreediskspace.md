---
title: Ivmharddisk hostfrediskspace-Eigenschaft (vpccominterfaces. h)
description: Ruft den verbleibenden Speicherplatz auf dem Host für die virtuelle Festplatte ab.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Hostfrediskspace-Eigenschaft virtueller PC
- Hostfrediskspace-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, hostfrediskspace-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105812"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="6f3be-106">Ivmharddisk:: hostfrediskspace-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f3be-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="6f3be-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f3be-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6f3be-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6f3be-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6f3be-109">Ruft den verbleibenden Speicherplatz auf dem Host für die virtuelle Festplatte ab.</span><span class="sxs-lookup"><span data-stu-id="6f3be-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="6f3be-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6f3be-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3be-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f3be-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="6f3be-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6f3be-112">Property value</span></span>

<span data-ttu-id="6f3be-113">Die Menge des verbleibenden Speicherplatzes, der auf dem Host Computer für die aktuelle Festplatten Abbild Datei verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6f3be-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="6f3be-114">Dieser Wert ist eine **Variante** vom Typ VT \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="6f3be-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f3be-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6f3be-115">Error codes</span></span>



| <span data-ttu-id="6f3be-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="6f3be-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6f3be-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6f3be-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f3be-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f3be-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="6f3be-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f3be-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="6f3be-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6f3be-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="6f3be-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6f3be-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6f3be-122"><dt>HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6f3be-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="6f3be-123">Der Pfad zur aktuellen virtuellen Festplatten Datei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6f3be-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6f3be-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6f3be-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="6f3be-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6f3be-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="6f3be-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f3be-126">Requirements</span></span>



| <span data-ttu-id="6f3be-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f3be-127">Requirement</span></span> | <span data-ttu-id="6f3be-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6f3be-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3be-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f3be-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3be-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f3be-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f3be-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f3be-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3be-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6f3be-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6f3be-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6f3be-133">End of client support</span></span><br/>    | <span data-ttu-id="6f3be-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f3be-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6f3be-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="6f3be-135">Product</span></span><br/>                  | <span data-ttu-id="6f3be-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6f3be-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6f3be-137">Header</span><span class="sxs-lookup"><span data-stu-id="6f3be-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f3be-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f3be-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6f3be-139">IID</span><span class="sxs-lookup"><span data-stu-id="6f3be-139">IID</span></span><br/>                      | <span data-ttu-id="6f3be-140">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="6f3be-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6f3be-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f3be-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3be-142">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="6f3be-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

