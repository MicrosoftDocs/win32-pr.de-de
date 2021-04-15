---
title: Ivmvirtualpc-Versions Eigenschaft (vpccominterfaces. h)
description: Ruft die Version dieser Instanz von Windows Virtual PC ab.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Versions Eigenschaft Virtual PC
- Versions Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, Version-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479221"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="3bfd8-106">Ivmvirtualpc:: Version-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3bfd8-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="3bfd8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3bfd8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3bfd8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3bfd8-109">Ruft die Version dieser Instanz von Windows Virtual PC ab.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="3bfd8-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bfd8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bfd8-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="3bfd8-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3bfd8-112">Property value</span></span>

<span data-ttu-id="3bfd8-113">Die Version.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3bfd8-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3bfd8-114">Error codes</span></span>



| <span data-ttu-id="3bfd8-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="3bfd8-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="3bfd8-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3bfd8-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3bfd8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3bfd8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="3bfd8-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3bfd8-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3bfd8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="3bfd8-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="3bfd8-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3bfd8-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="3bfd8-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3bfd8-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3bfd8-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="3bfd8-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="3bfd8-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3bfd8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bfd8-125">Remarks</span></span>

<span data-ttu-id="3bfd8-126">Die Informationen zur Windows Virtual PC-Version werden als Zeichen folgen Wert im folgenden Format zurückgegeben: "*v*. *s*. *BBB*. *Tee*", wobei *v* die Hauptversionsnummer ist, *s* die neben Versionsnummer, *BBB* die Buildnummer, *t* der Buildtyp (0 = Releasebuild) und *EE* die Server Edition (SE = Standard Edition, EE = Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="3bfd8-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bfd8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bfd8-127">Requirements</span></span>



| <span data-ttu-id="3bfd8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bfd8-128">Requirement</span></span> | <span data-ttu-id="3bfd8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3bfd8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bfd8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bfd8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3bfd8-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bfd8-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bfd8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bfd8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3bfd8-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3bfd8-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3bfd8-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3bfd8-134">End of client support</span></span><br/>    | <span data-ttu-id="3bfd8-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3bfd8-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3bfd8-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="3bfd8-136">Product</span></span><br/>                  | <span data-ttu-id="3bfd8-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3bfd8-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3bfd8-138">Header</span><span class="sxs-lookup"><span data-stu-id="3bfd8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bfd8-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bfd8-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3bfd8-140">IID</span><span class="sxs-lookup"><span data-stu-id="3bfd8-140">IID</span></span><br/>                      | <span data-ttu-id="3bfd8-141">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="3bfd8-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3bfd8-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bfd8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bfd8-143">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="3bfd8-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

