---
title: Ivmtaskcollection-_NewEnum-Eigenschaft (vpccominterfaces. h)
description: Ruft einen Enumerator für die Auflistung ab. | Ivmtaskcollection-_NewEnum-Eigenschaft (vpccominterfaces. h)
ms.assetid: 15c36bdb-5d26-4f67-aa7e-73b9bde2aa22
keywords:
- Virtual PC für _NewEnum-Eigenschaft
- _NewEnum-Eigenschaft Virtual PC, ivmtaskcollection-Schnittstelle
- Ivmtaskcollection-Schnittstelle Virtual PC, _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTaskCollection._NewEnum
- IVMTaskCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5efe2d581448b815095aafb5c5910be1997165
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361809"
---
# <a name="ivmtaskcollection_newenum-property"></a><span data-ttu-id="2874b-107">Ivmtaskcollection:: \_ netwenum-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2874b-107">IVMTaskCollection::\_NewEnum property</span></span>

<span data-ttu-id="2874b-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2874b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2874b-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2874b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2874b-110">Ruft einen Enumerator für die Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="2874b-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="2874b-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2874b-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2874b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="2874b-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="2874b-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2874b-113">Property value</span></span>

<span data-ttu-id="2874b-114">Der [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerator.</span><span class="sxs-lookup"><span data-stu-id="2874b-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2874b-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2874b-115">Error codes</span></span>



| <span data-ttu-id="2874b-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="2874b-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2874b-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2874b-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="2874b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2874b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2874b-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2874b-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="2874b-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2874b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2874b-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2874b-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="2874b-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2874b-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2874b-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2874b-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2874b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2874b-124">Requirements</span></span>



| <span data-ttu-id="2874b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2874b-125">Requirement</span></span> | <span data-ttu-id="2874b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2874b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2874b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2874b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2874b-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2874b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2874b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2874b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2874b-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2874b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2874b-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2874b-131">End of client support</span></span><br/>    | <span data-ttu-id="2874b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2874b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2874b-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="2874b-133">Product</span></span><br/>                  | <span data-ttu-id="2874b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2874b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2874b-135">Header</span><span class="sxs-lookup"><span data-stu-id="2874b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2874b-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2874b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2874b-137">IID</span><span class="sxs-lookup"><span data-stu-id="2874b-137">IID</span></span><br/>                      | <span data-ttu-id="2874b-138">IID \_ ivmtaskcollection ist definiert als 5c4387c8-0e8b-4b97-8058-84679adf 4c40</span><span class="sxs-lookup"><span data-stu-id="2874b-138">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2874b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2874b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2874b-140">**Ivmtaskcollection**</span><span class="sxs-lookup"><span data-stu-id="2874b-140">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

