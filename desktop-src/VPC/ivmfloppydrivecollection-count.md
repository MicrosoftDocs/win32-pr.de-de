---
title: Ivmfloppydrivecollection Count-Eigenschaft (vpccominterfaces. h)
description: Anzahl der Diskettenlaufwerke in dieser Sammlung.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmfloppydrivecollection-Schnittstelle
- Ivmfloppydrivecollection Interface Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b00c13795a633c664cea2c4476d58b346f9108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040969"
---
# <a name="ivmfloppydrivecollectioncount-property"></a><span data-ttu-id="66da1-106">Ivmfloppydrivecollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66da1-106">IVMFloppyDriveCollection::Count property</span></span>

<span data-ttu-id="66da1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66da1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66da1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66da1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66da1-109">Ruft die Anzahl der Diskettenlaufwerke in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="66da1-109">Retrieves the number of floppy drives in this collection.</span></span>

<span data-ttu-id="66da1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="66da1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66da1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="66da1-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="66da1-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="66da1-112">Property value</span></span>

<span data-ttu-id="66da1-113">Die Anzahl der Disketten Medien Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="66da1-113">The number of floppy media drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66da1-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="66da1-114">Error codes</span></span>



| <span data-ttu-id="66da1-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="66da1-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="66da1-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="66da1-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="66da1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66da1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="66da1-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="66da1-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="66da1-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66da1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="66da1-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="66da1-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="66da1-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="66da1-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="66da1-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="66da1-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="66da1-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="66da1-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="66da1-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="66da1-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="66da1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66da1-125">Requirements</span></span>



| <span data-ttu-id="66da1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66da1-126">Requirement</span></span> | <span data-ttu-id="66da1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="66da1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66da1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66da1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66da1-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66da1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66da1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66da1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66da1-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="66da1-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66da1-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="66da1-132">End of client support</span></span><br/>    | <span data-ttu-id="66da1-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66da1-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66da1-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="66da1-134">Product</span></span><br/>                  | <span data-ttu-id="66da1-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66da1-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66da1-136">Header</span><span class="sxs-lookup"><span data-stu-id="66da1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="66da1-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66da1-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66da1-138">IID</span><span class="sxs-lookup"><span data-stu-id="66da1-138">IID</span></span><br/>                      | <span data-ttu-id="66da1-139">IID \_ ivmfloppydrivecollection ist als 8ba70a25-s698-4ee5-85ce-3cc93a925516 definiert.</span><span class="sxs-lookup"><span data-stu-id="66da1-139">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="66da1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66da1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66da1-141">**Ivmfloppydrivecollection**</span><span class="sxs-lookup"><span data-stu-id="66da1-141">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

