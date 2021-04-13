---
title: Ivmtaskcollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das Task-Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmtaskcollection-Schnittstelle
- Ivmtaskcollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518386"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="66183-106">Ivmtaskcollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66183-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="66183-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66183-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66183-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66183-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66183-109">Ruft das Task-Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="66183-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="66183-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="66183-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66183-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="66183-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="66183-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="66183-112">Property value</span></span>

<span data-ttu-id="66183-113">Das [**ivmtask**](ivmtask.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="66183-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66183-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="66183-114">Error codes</span></span>



| <span data-ttu-id="66183-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="66183-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="66183-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="66183-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66183-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66183-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="66183-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="66183-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="66183-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66183-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="66183-120">Der *Aufgaben* Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="66183-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="66183-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="66183-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="66183-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="66183-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="66183-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="66183-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="66183-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="66183-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="66183-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66183-125">Requirements</span></span>



| <span data-ttu-id="66183-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66183-126">Requirement</span></span> | <span data-ttu-id="66183-127">Wert</span><span class="sxs-lookup"><span data-stu-id="66183-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66183-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66183-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66183-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66183-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66183-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66183-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66183-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="66183-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66183-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="66183-132">End of client support</span></span><br/>    | <span data-ttu-id="66183-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66183-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66183-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="66183-134">Product</span></span><br/>                  | <span data-ttu-id="66183-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66183-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66183-136">Header</span><span class="sxs-lookup"><span data-stu-id="66183-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="66183-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66183-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66183-138">IID</span><span class="sxs-lookup"><span data-stu-id="66183-138">IID</span></span><br/>                      | <span data-ttu-id="66183-139">IID \_ ivmtaskcollection ist definiert als 5c4387c8-0e8b-4b97-8058-84679adf 4c40</span><span class="sxs-lookup"><span data-stu-id="66183-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="66183-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66183-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66183-141">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="66183-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="66183-142">**Ivmtaskcollection**</span><span class="sxs-lookup"><span data-stu-id="66183-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

