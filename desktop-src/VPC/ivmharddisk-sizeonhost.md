---
title: Ivmharddisk sizeonhost-Eigenschaft (vpccominterfaces. h)
description: Größe der virtuellen Festplatten Datei auf dem Host Computer.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Sizeonhost-Eigenschaft virtueller PC
- Sizeonhost-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, sizeonhost (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040819"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="ce704-106">Ivmharddisk:: sizeonhost (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce704-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="ce704-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce704-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce704-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ce704-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce704-109">Ruft die Größe der virtuellen Festplatten Datei auf dem Host Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ce704-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="ce704-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ce704-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce704-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce704-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="ce704-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ce704-112">Property value</span></span>

<span data-ttu-id="ce704-113">Die Größe der Festplatten Abbild Datei in Byte.</span><span class="sxs-lookup"><span data-stu-id="ce704-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="ce704-114">Dieser Wert ist eine **Variante** vom Typ **VT \_ Decimal**.</span><span class="sxs-lookup"><span data-stu-id="ce704-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce704-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ce704-115">Error codes</span></span>



| <span data-ttu-id="ce704-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="ce704-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="ce704-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce704-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="ce704-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ce704-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="ce704-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce704-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="ce704-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ce704-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="ce704-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ce704-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="ce704-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ce704-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="ce704-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ce704-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="ce704-124"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="ce704-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="ce704-125">Die Festplatten Abbild Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ce704-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ce704-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce704-126">Requirements</span></span>



| <span data-ttu-id="ce704-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce704-127">Requirement</span></span> | <span data-ttu-id="ce704-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ce704-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce704-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce704-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ce704-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce704-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce704-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce704-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ce704-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ce704-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce704-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ce704-133">End of client support</span></span><br/>    | <span data-ttu-id="ce704-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce704-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce704-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="ce704-135">Product</span></span><br/>                  | <span data-ttu-id="ce704-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce704-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce704-137">Header</span><span class="sxs-lookup"><span data-stu-id="ce704-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce704-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce704-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ce704-139">IID</span><span class="sxs-lookup"><span data-stu-id="ce704-139">IID</span></span><br/>                      | <span data-ttu-id="ce704-140">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="ce704-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ce704-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce704-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce704-142">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="ce704-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

