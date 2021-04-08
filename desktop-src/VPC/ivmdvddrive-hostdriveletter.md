---
title: Ivmdvddrive-hostdriveletter-Eigenschaft (vpccominterfaces. h)
description: Der Buchstabe des Host Laufwerks, das für dieses Gerät festgelegt ist.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Hostdriveletter-Eigenschaft virtueller PC
- Hostdriveletter-Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, hostdriveletter (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741096"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="464ff-106">Ivmdvddrive:: hostdriveletter (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="464ff-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="464ff-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="464ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="464ff-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="464ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="464ff-109">Ruft den Buchstaben des Host Laufwerks ab, das für dieses Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="464ff-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="464ff-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="464ff-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="464ff-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="464ff-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="464ff-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="464ff-112">Property value</span></span>

<span data-ttu-id="464ff-113">Der Laufwerk Buchstabe.</span><span class="sxs-lookup"><span data-stu-id="464ff-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="464ff-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="464ff-114">Error codes</span></span>



| <span data-ttu-id="464ff-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="464ff-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="464ff-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="464ff-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="464ff-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="464ff-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="464ff-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="464ff-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="464ff-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="464ff-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="464ff-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="464ff-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="464ff-121"><dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="464ff-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="464ff-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="464ff-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="464ff-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="464ff-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="464ff-124">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="464ff-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="464ff-125"><dt>VM \_ E \_ Medien \_ falscher \_ Typ</dt> <dt>0xa00400728</dt></span><span class="sxs-lookup"><span data-stu-id="464ff-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="464ff-126">Die von diesem DVD-Laufwerk erfassten Medien sind kein Host Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="464ff-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="464ff-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="464ff-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="464ff-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="464ff-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="464ff-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="464ff-129">Requirements</span></span>



| <span data-ttu-id="464ff-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="464ff-130">Requirement</span></span> | <span data-ttu-id="464ff-131">Wert</span><span class="sxs-lookup"><span data-stu-id="464ff-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="464ff-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="464ff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="464ff-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464ff-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="464ff-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="464ff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="464ff-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="464ff-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="464ff-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="464ff-136">End of client support</span></span><br/>    | <span data-ttu-id="464ff-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="464ff-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="464ff-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="464ff-138">Product</span></span><br/>                  | <span data-ttu-id="464ff-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="464ff-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="464ff-140">Header</span><span class="sxs-lookup"><span data-stu-id="464ff-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="464ff-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="464ff-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="464ff-142">IID</span><span class="sxs-lookup"><span data-stu-id="464ff-142">IID</span></span><br/>                      | <span data-ttu-id="464ff-143">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="464ff-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="464ff-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="464ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464ff-145">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="464ff-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

