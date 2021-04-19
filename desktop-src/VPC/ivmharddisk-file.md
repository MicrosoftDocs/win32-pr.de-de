---
title: Ivmharddisk-Datei Eigenschaft (vpccominterfaces. h)
description: Ruft den vollständigen Pfadnamen der virtuellen Festplatten Datei ab.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Datei Eigenschaft virtueller PC
- Datei Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, File-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346332"
---
# <a name="ivmharddiskfile-property"></a><span data-ttu-id="4baba-106">Ivmharddisk:: File (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4baba-106">IVMHardDisk::File property</span></span>

<span data-ttu-id="4baba-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4baba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4baba-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4baba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4baba-109">Ruft den vollständigen Pfadnamen der virtuellen Festplatten Datei ab.</span><span class="sxs-lookup"><span data-stu-id="4baba-109">Retrieves the full path name of the virtual hard disk file.</span></span>

<span data-ttu-id="4baba-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4baba-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4baba-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4baba-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a><span data-ttu-id="4baba-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4baba-112">Property value</span></span>

<span data-ttu-id="4baba-113">Der vollständige Pfadname der aktuellen Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="4baba-113">The full path name of the current hard disk image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4baba-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4baba-114">Error codes</span></span>



| <span data-ttu-id="4baba-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="4baba-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4baba-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4baba-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4baba-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4baba-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4baba-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4baba-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4baba-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4baba-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4baba-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="4baba-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4baba-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4baba-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4baba-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4baba-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4baba-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4baba-123">Requirements</span></span>



| <span data-ttu-id="4baba-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4baba-124">Requirement</span></span> | <span data-ttu-id="4baba-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4baba-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4baba-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4baba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4baba-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4baba-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4baba-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4baba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4baba-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4baba-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4baba-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4baba-130">End of client support</span></span><br/>    | <span data-ttu-id="4baba-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4baba-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4baba-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="4baba-132">Product</span></span><br/>                  | <span data-ttu-id="4baba-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4baba-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4baba-134">Header</span><span class="sxs-lookup"><span data-stu-id="4baba-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4baba-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4baba-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4baba-136">IID</span><span class="sxs-lookup"><span data-stu-id="4baba-136">IID</span></span><br/>                      | <span data-ttu-id="4baba-137">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="4baba-137">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4baba-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4baba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4baba-139">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="4baba-139">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

