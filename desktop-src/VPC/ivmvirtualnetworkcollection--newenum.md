---
title: Ivmvirtualnetworkcollection-_NewEnum-Eigenschaft (vpccominterfaces. h)
description: Ruft einen Enumerator für die Auflistung ab. | Ivmvirtualnetworkcollection-_NewEnum-Eigenschaft (vpccominterfaces. h)
ms.assetid: 3ea01a88-72ec-4dc0-901f-e48092cf9251
keywords:
- Virtual PC für _NewEnum-Eigenschaft
- _NewEnum-Eigenschaft Virtual PC, ivmvirtualnetworkcollection-Schnittstelle
- Ivmvirtualnetworkcollection Interface Virtual PC, _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection._NewEnum
- IVMVirtualNetworkCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50a279e3f160a79f143a7516e29c0dbc3eccdf4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219390"
---
# <a name="ivmvirtualnetworkcollection_newenum-property"></a><span data-ttu-id="b7c46-107">Ivmvirtualnetworkcollection:: \_ netwenum-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7c46-107">IVMVirtualNetworkCollection::\_NewEnum property</span></span>

<span data-ttu-id="b7c46-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7c46-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7c46-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b7c46-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7c46-110">Ruft einen Enumerator für die Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="b7c46-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="b7c46-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b7c46-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c46-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c46-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="b7c46-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b7c46-113">Property value</span></span>

<span data-ttu-id="b7c46-114">Der [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerator.</span><span class="sxs-lookup"><span data-stu-id="b7c46-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7c46-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b7c46-115">Error codes</span></span>



| <span data-ttu-id="b7c46-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="b7c46-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b7c46-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b7c46-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="b7c46-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7c46-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b7c46-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7c46-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="b7c46-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b7c46-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b7c46-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b7c46-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="b7c46-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b7c46-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b7c46-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b7c46-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b7c46-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7c46-124">Requirements</span></span>



| <span data-ttu-id="b7c46-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7c46-125">Requirement</span></span> | <span data-ttu-id="b7c46-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c46-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c46-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7c46-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c46-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7c46-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7c46-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7c46-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c46-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b7c46-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b7c46-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b7c46-131">End of client support</span></span><br/>    | <span data-ttu-id="b7c46-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7c46-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="b7c46-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="b7c46-133">Product</span></span><br/>                  | <span data-ttu-id="b7c46-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7c46-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="b7c46-135">Header</span><span class="sxs-lookup"><span data-stu-id="b7c46-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7c46-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c46-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="b7c46-137">IID</span><span class="sxs-lookup"><span data-stu-id="b7c46-137">IID</span></span><br/>                      | <span data-ttu-id="b7c46-138">IID \_ ivmvirtualnetworkcollection ist als 8ed680be-4242-4b2a-A21C-1982d8b0f. definiert.</span><span class="sxs-lookup"><span data-stu-id="b7c46-138">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7c46-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7c46-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c46-140">**Ivmvirtualnetworkcollection**</span><span class="sxs-lookup"><span data-stu-id="b7c46-140">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

