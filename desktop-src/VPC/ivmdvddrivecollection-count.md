---
title: Ivmdvddrivecollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der CD-und DVD-Laufwerke in dieser Auflistung ab.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmdvddrivecollection-Schnittstelle
- Ivmdvddrivecollection Interface Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339338"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="581f2-106">Ivmdvddrivecollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="581f2-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="581f2-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="581f2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="581f2-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="581f2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="581f2-109">Ruft die Anzahl der CD-und DVD-Laufwerke in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="581f2-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="581f2-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="581f2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="581f2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="581f2-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="581f2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="581f2-112">Property value</span></span>

<span data-ttu-id="581f2-113">Die Anzahl von CD-und DVD-Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="581f2-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="581f2-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="581f2-114">Error codes</span></span>



| <span data-ttu-id="581f2-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="581f2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="581f2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="581f2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="581f2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="581f2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="581f2-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="581f2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="581f2-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="581f2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="581f2-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="581f2-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="581f2-121"><dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="581f2-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="581f2-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="581f2-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="581f2-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="581f2-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="581f2-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="581f2-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="581f2-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="581f2-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="581f2-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="581f2-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="581f2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="581f2-127">Requirements</span></span>



| <span data-ttu-id="581f2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="581f2-128">Requirement</span></span> | <span data-ttu-id="581f2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="581f2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="581f2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="581f2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="581f2-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="581f2-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="581f2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="581f2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="581f2-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="581f2-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="581f2-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="581f2-134">End of client support</span></span><br/>    | <span data-ttu-id="581f2-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="581f2-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="581f2-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="581f2-136">Product</span></span><br/>                  | <span data-ttu-id="581f2-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="581f2-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="581f2-138">Header</span><span class="sxs-lookup"><span data-stu-id="581f2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="581f2-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="581f2-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="581f2-140">IID</span><span class="sxs-lookup"><span data-stu-id="581f2-140">IID</span></span><br/>                      | <span data-ttu-id="581f2-141">IID \_ ivmdvddrivecollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.</span><span class="sxs-lookup"><span data-stu-id="581f2-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="581f2-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="581f2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581f2-143">**Ivmdvddrivecollection**</span><span class="sxs-lookup"><span data-stu-id="581f2-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

