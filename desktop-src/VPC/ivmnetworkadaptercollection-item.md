---
title: Ivmnetworkadaptercollection-Element Eigenschaft (vpccominterfaces. h)
description: Ivmnetworkadapter-Objekt, das dem angegebenen Index entspricht.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmnetworkadaptercollection-Schnittstelle
- Ivmnetworkadaptercollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957117"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="6b190-106">Ivmnetworkadaptercollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6b190-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="6b190-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b190-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6b190-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6b190-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6b190-109">Ruft das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="6b190-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="6b190-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6b190-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b190-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b190-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="6b190-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6b190-112">Property value</span></span>

<span data-ttu-id="6b190-113">Das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b190-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b190-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6b190-114">Error codes</span></span>



| <span data-ttu-id="6b190-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="6b190-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6b190-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b190-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b190-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6b190-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6b190-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b190-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="6b190-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6b190-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6b190-120">Der *NetworkInterface* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6b190-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="6b190-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="6b190-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="6b190-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6b190-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="6b190-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6b190-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6b190-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6b190-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="6b190-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b190-125">Requirements</span></span>



| <span data-ttu-id="6b190-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b190-126">Requirement</span></span> | <span data-ttu-id="6b190-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6b190-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b190-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b190-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6b190-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b190-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b190-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b190-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6b190-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6b190-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6b190-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6b190-132">End of client support</span></span><br/>    | <span data-ttu-id="6b190-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b190-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="6b190-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="6b190-134">Product</span></span><br/>                  | <span data-ttu-id="6b190-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6b190-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="6b190-136">Header</span><span class="sxs-lookup"><span data-stu-id="6b190-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b190-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b190-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="6b190-138">IID</span><span class="sxs-lookup"><span data-stu-id="6b190-138">IID</span></span><br/>                      | <span data-ttu-id="6b190-139">IID \_ ivmnetworkadaptercollection ist als ebaeafe9-EBCD-47cf-866e-ad87d735e479 definiert.</span><span class="sxs-lookup"><span data-stu-id="6b190-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b190-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b190-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b190-141">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="6b190-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="6b190-142">**Ivmnetworkadaptercollection**</span><span class="sxs-lookup"><span data-stu-id="6b190-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

