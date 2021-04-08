---
title: Ivmharddiskconnectioncollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der Festplatten Verbindungen in dieser Sammlung ab.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmharddiskconnectioncollection-Schnittstelle
- Ivmharddiskconnectioncollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741753"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="58ecb-106">Ivmharddiskconnectioncollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="58ecb-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="58ecb-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58ecb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="58ecb-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="58ecb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="58ecb-109">Ruft die Anzahl der Festplatten Verbindungen in dieser Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="58ecb-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="58ecb-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="58ecb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ecb-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="58ecb-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="58ecb-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="58ecb-112">Property value</span></span>

<span data-ttu-id="58ecb-113">Die Anzahl der Festplatten Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="58ecb-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="58ecb-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="58ecb-114">Error codes</span></span>



| <span data-ttu-id="58ecb-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="58ecb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="58ecb-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58ecb-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="58ecb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58ecb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="58ecb-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="58ecb-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="58ecb-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="58ecb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="58ecb-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="58ecb-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="58ecb-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="58ecb-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="58ecb-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="58ecb-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="58ecb-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="58ecb-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="58ecb-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="58ecb-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="58ecb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58ecb-125">Requirements</span></span>



| <span data-ttu-id="58ecb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58ecb-126">Requirement</span></span> | <span data-ttu-id="58ecb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="58ecb-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ecb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58ecb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="58ecb-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58ecb-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="58ecb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58ecb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="58ecb-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="58ecb-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="58ecb-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="58ecb-132">End of client support</span></span><br/>    | <span data-ttu-id="58ecb-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58ecb-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="58ecb-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="58ecb-134">Product</span></span><br/>                  | <span data-ttu-id="58ecb-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="58ecb-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="58ecb-136">Header</span><span class="sxs-lookup"><span data-stu-id="58ecb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ecb-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ecb-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="58ecb-138">IID</span><span class="sxs-lookup"><span data-stu-id="58ecb-138">IID</span></span><br/>                      | <span data-ttu-id="58ecb-139">IID \_ ivmharddiskconnectioncollection ist definiert als b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="58ecb-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58ecb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58ecb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ecb-141">**Ivmharddiskconnectioncollection**</span><span class="sxs-lookup"><span data-stu-id="58ecb-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

