---
title: Ivmdvddrivecollection-_NewEnum Eigenschaft (vpccominterfaces. h)
description: Ruft einen Enumerator für die CD/DVD-Auflistung ab.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- Virtual PC für _NewEnum-Eigenschaft
- _NewEnum-Eigenschaft Virtual PC, ivmdvddrivecollection-Schnittstelle
- Ivmdvddrivecollection Interface Virtual PC, _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949830"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="ccff9-106">Ivmdvddrivecollection:: \_ netwenum-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ccff9-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="ccff9-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ccff9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ccff9-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ccff9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ccff9-109">Ruft einen Enumerator für die CD/DVD-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="ccff9-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="ccff9-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ccff9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccff9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccff9-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="ccff9-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ccff9-112">Property value</span></span>

<span data-ttu-id="ccff9-113">Der [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerator.</span><span class="sxs-lookup"><span data-stu-id="ccff9-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccff9-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ccff9-114">Error codes</span></span>



| <span data-ttu-id="ccff9-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="ccff9-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ccff9-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ccff9-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ccff9-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ccff9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ccff9-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccff9-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ccff9-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ccff9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ccff9-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ccff9-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ccff9-121"><dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="ccff9-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="ccff9-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ccff9-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="ccff9-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ccff9-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ccff9-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ccff9-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="ccff9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccff9-125">Requirements</span></span>



| <span data-ttu-id="ccff9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccff9-126">Requirement</span></span> | <span data-ttu-id="ccff9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ccff9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccff9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccff9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ccff9-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccff9-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccff9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccff9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ccff9-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ccff9-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ccff9-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ccff9-132">End of client support</span></span><br/>    | <span data-ttu-id="ccff9-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccff9-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ccff9-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="ccff9-134">Product</span></span><br/>                  | <span data-ttu-id="ccff9-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ccff9-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ccff9-136">Header</span><span class="sxs-lookup"><span data-stu-id="ccff9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccff9-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccff9-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ccff9-138">IID</span><span class="sxs-lookup"><span data-stu-id="ccff9-138">IID</span></span><br/>                      | <span data-ttu-id="ccff9-139">IID \_ ivmdvddrivecollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.</span><span class="sxs-lookup"><span data-stu-id="ccff9-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ccff9-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccff9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccff9-141">**Ivmdvddrivecollection**</span><span class="sxs-lookup"><span data-stu-id="ccff9-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

