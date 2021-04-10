---
title: Ivmvirtualnetworkcollection-Element Eigenschaft (vpccominterfaces. h)
description: Ivmvirtualnetwork-Objekt, das dem angegebenen Index entspricht.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmvirtualnetworkcollection-Schnittstelle
- Ivmvirtualnetworkcollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040700"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a><span data-ttu-id="c75ef-106">Ivmvirtualnetworkcollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c75ef-106">IVMVirtualNetworkCollection::Item property</span></span>

<span data-ttu-id="c75ef-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c75ef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c75ef-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c75ef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c75ef-109">Ruft das [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="c75ef-109">Retrieves the [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="c75ef-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c75ef-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75ef-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c75ef-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="c75ef-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c75ef-112">Property value</span></span>

<span data-ttu-id="c75ef-113">Das [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c75ef-113">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c75ef-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c75ef-114">Error codes</span></span>



| <span data-ttu-id="c75ef-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c75ef-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c75ef-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c75ef-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c75ef-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c75ef-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c75ef-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c75ef-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="c75ef-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c75ef-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c75ef-120">Der *VirtualNetwork* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c75ef-120">The *virtualNetwork* parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c75ef-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="c75ef-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="c75ef-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c75ef-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="c75ef-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c75ef-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c75ef-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c75ef-124">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="c75ef-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c75ef-125">Requirements</span></span>



| <span data-ttu-id="c75ef-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c75ef-126">Requirement</span></span> | <span data-ttu-id="c75ef-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c75ef-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c75ef-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c75ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c75ef-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c75ef-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c75ef-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c75ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c75ef-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c75ef-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c75ef-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c75ef-132">End of client support</span></span><br/>    | <span data-ttu-id="c75ef-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c75ef-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="c75ef-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="c75ef-134">Product</span></span><br/>                  | <span data-ttu-id="c75ef-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c75ef-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="c75ef-136">Header</span><span class="sxs-lookup"><span data-stu-id="c75ef-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75ef-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c75ef-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="c75ef-138">IID</span><span class="sxs-lookup"><span data-stu-id="c75ef-138">IID</span></span><br/>                      | <span data-ttu-id="c75ef-139">IID \_ ivmvirtualnetworkcollection ist als 8ed680be-4242-4b2a-A21C-1982d8b0f. definiert.</span><span class="sxs-lookup"><span data-stu-id="c75ef-139">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c75ef-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c75ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75ef-141">**Ivmvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="c75ef-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> <dt>

[<span data-ttu-id="c75ef-142">**Ivmvirtualnetworkcollection**</span><span class="sxs-lookup"><span data-stu-id="c75ef-142">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

