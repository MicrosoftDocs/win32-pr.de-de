---
title: Ivmtaskcollection-Anzahl (Eigenschaft) (vpccominterfaces. h)
description: Ruft die Anzahl der Tasks in dieser Auflistung ab.
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmtaskcollection-Schnittstelle
- Ivmtaskcollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859082"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="9a656-106">Ivmtaskcollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9a656-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="9a656-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a656-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9a656-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9a656-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9a656-109">Ruft die Anzahl der Tasks in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="9a656-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="9a656-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9a656-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a656-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a656-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="9a656-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9a656-112">Property value</span></span>

<span data-ttu-id="9a656-113">Die Anzahl der Tasks.</span><span class="sxs-lookup"><span data-stu-id="9a656-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a656-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9a656-114">Error codes</span></span>



| <span data-ttu-id="9a656-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="9a656-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="9a656-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9a656-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9a656-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9a656-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9a656-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a656-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="9a656-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9a656-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9a656-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="9a656-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="9a656-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9a656-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9a656-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9a656-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9a656-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a656-123">Requirements</span></span>



| <span data-ttu-id="9a656-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a656-124">Requirement</span></span> | <span data-ttu-id="9a656-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9a656-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a656-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a656-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9a656-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a656-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a656-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a656-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9a656-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9a656-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9a656-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9a656-130">End of client support</span></span><br/>    | <span data-ttu-id="9a656-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a656-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9a656-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="9a656-132">Product</span></span><br/>                  | <span data-ttu-id="9a656-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9a656-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9a656-134">Header</span><span class="sxs-lookup"><span data-stu-id="9a656-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a656-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a656-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9a656-136">IID</span><span class="sxs-lookup"><span data-stu-id="9a656-136">IID</span></span><br/>                      | <span data-ttu-id="9a656-137">IID \_ ivmtaskcollection ist definiert als 5c4387c8-0e8b-4b97-8058-84679adf 4c40</span><span class="sxs-lookup"><span data-stu-id="9a656-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9a656-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a656-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a656-139">**Ivmtaskcollection**</span><span class="sxs-lookup"><span data-stu-id="9a656-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

