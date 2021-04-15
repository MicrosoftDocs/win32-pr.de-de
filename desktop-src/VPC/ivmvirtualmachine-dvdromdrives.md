---
title: Ivmvirtualmachine dvdromdrives-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Sammlung von CD-und DVD-Laufwerken ab, die an den virtuellen Computer angefügt sind.
ms.assetid: e9e7d912-568f-4a3d-85cf-63f6fa99cb19
keywords:
- Dvdromdrives-Eigenschaft virtueller PC
- Dvdromdrives-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, dvdromdrives (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DVDROMDrives
- IVMVirtualMachine.get_DVDROMDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9980d783b19bfef7ce5437253b7923d6e6a2ebf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518788"
---
# <a name="ivmvirtualmachinedvdromdrives-property"></a><span data-ttu-id="6b2b5-106">Ivmvirtualmachine::D vdromdrives (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6b2b5-106">IVMVirtualMachine::DVDROMDrives property</span></span>

<span data-ttu-id="6b2b5-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6b2b5-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6b2b5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6b2b5-109">Ruft eine Aufzähl Bare Sammlung von CD-und DVD-Laufwerken ab, die an den virtuellen Computer angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-109">Retrieves an enumerable collection of CD and DVD drives attached to the virtual machine.</span></span>

<span data-ttu-id="6b2b5-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2b5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2b5-111">Syntax</span></span>


```C++
HRESULT get_DVDROMDrives(
  [out, retval] IVMDVDDriveCollection **dvdROMCollection
);
```



## <a name="property-value"></a><span data-ttu-id="6b2b5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6b2b5-112">Property value</span></span>

<span data-ttu-id="6b2b5-113">Ein [**ivmdvddrivecollection**](ivmdvddrivecollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-113">An [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b2b5-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6b2b5-114">Error codes</span></span>



| <span data-ttu-id="6b2b5-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="6b2b5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6b2b5-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b2b5-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6b2b5-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6b2b5-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="6b2b5-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6b2b5-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="6b2b5-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b5-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6b2b5-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="6b2b5-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b5-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6b2b5-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6b2b5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b2b5-125">Requirements</span></span>



| <span data-ttu-id="6b2b5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b2b5-126">Requirement</span></span> | <span data-ttu-id="6b2b5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6b2b5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2b5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b2b5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2b5-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b2b5-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b2b5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b2b5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2b5-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6b2b5-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6b2b5-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6b2b5-132">End of client support</span></span><br/>    | <span data-ttu-id="6b2b5-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b2b5-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6b2b5-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="6b2b5-134">Product</span></span><br/>                  | <span data-ttu-id="6b2b5-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6b2b5-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6b2b5-136">Header</span><span class="sxs-lookup"><span data-stu-id="6b2b5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b2b5-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b5-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6b2b5-138">IID</span><span class="sxs-lookup"><span data-stu-id="6b2b5-138">IID</span></span><br/>                      | <span data-ttu-id="6b2b5-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="6b2b5-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6b2b5-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b2b5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2b5-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="6b2b5-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

