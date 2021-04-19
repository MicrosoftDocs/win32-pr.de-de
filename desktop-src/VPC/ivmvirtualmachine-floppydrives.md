---
title: Ivmvirtualmachine floppydrives-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von Diskettenlaufwerken ab, die an den virtuellen Computer angefügt sind.
ms.assetid: 8b8ea1c7-77c3-46b6-ab0b-0c7b4ab387ae
keywords:
- Floppydrives-Eigenschaft virtueller PC
- Floppydrives-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, floppydrives (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.FloppyDrives
- IVMVirtualMachine.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4ec942d55c3d98b3d45a013fb1142ea097edfca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339587"
---
# <a name="ivmvirtualmachinefloppydrives-property"></a><span data-ttu-id="a150b-106">Ivmvirtualmachine:: floppydrives (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a150b-106">IVMVirtualMachine::FloppyDrives property</span></span>

<span data-ttu-id="a150b-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a150b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a150b-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a150b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a150b-109">Ruft eine Aufzähl Bare Auflistung von Diskettenlaufwerken ab, die an den virtuellen Computer angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="a150b-109">Retrieves an enumerable collection of floppy drives attached to the virtual machine.</span></span>

<span data-ttu-id="a150b-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a150b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a150b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a150b-111">Syntax</span></span>


```C++
HRESULT get_FloppyDrives(
  [out, retval] IVMFloppyDriveCollection **floppyCollection
);
```



## <a name="property-value"></a><span data-ttu-id="a150b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a150b-112">Property value</span></span>

<span data-ttu-id="a150b-113">Ein [**ivmfloppydrivecollection**](ivmfloppydrivecollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a150b-113">An [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a150b-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a150b-114">Error codes</span></span>



| <span data-ttu-id="a150b-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a150b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a150b-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a150b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a150b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a150b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a150b-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a150b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a150b-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a150b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a150b-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a150b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a150b-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="a150b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a150b-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a150b-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a150b-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a150b-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a150b-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a150b-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a150b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a150b-125">Requirements</span></span>



| <span data-ttu-id="a150b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a150b-126">Requirement</span></span> | <span data-ttu-id="a150b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a150b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a150b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a150b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a150b-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a150b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a150b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a150b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a150b-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a150b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a150b-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a150b-132">End of client support</span></span><br/>    | <span data-ttu-id="a150b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a150b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a150b-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="a150b-134">Product</span></span><br/>                  | <span data-ttu-id="a150b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a150b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a150b-136">Header</span><span class="sxs-lookup"><span data-stu-id="a150b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a150b-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a150b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a150b-138">IID</span><span class="sxs-lookup"><span data-stu-id="a150b-138">IID</span></span><br/>                      | <span data-ttu-id="a150b-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="a150b-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a150b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a150b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a150b-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="a150b-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

