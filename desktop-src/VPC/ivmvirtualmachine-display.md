---
title: Ivmvirtualmachine-Anzeige Eigenschaft (vpccominterfaces. h)
description: Ruft die Videoanzeige für den virtuellen Computer ab.
ms.assetid: ca5a433d-4613-4b6d-9de7-d9c6a2038e38
keywords:
- Anzeigen der Eigenschaft virtueller PC
- Anzeigen der Eigenschaft Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, Display-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Display
- IVMVirtualMachine.get_Display
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175150ba76074918d497efd2c9f65a53af46b8bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477406"
---
# <a name="ivmvirtualmachinedisplay-property"></a><span data-ttu-id="c296e-106">Ivmvirtualmachine::D isplay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c296e-106">IVMVirtualMachine::Display property</span></span>

<span data-ttu-id="c296e-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c296e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c296e-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c296e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c296e-109">Ruft die Videoanzeige für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="c296e-109">Retrieves the video display for the virtual machine.</span></span>

<span data-ttu-id="c296e-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c296e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c296e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c296e-111">Syntax</span></span>


```C++
HRESULT get_Display(
  [out, retval] IVMDisplay **display
);
```



## <a name="property-value"></a><span data-ttu-id="c296e-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c296e-112">Property value</span></span>

<span data-ttu-id="c296e-113">Das [**ivmdisplay**](ivmdisplay.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c296e-113">The [**IVMDisplay**](ivmdisplay.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c296e-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c296e-114">Error codes</span></span>



| <span data-ttu-id="c296e-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c296e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c296e-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c296e-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c296e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c296e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c296e-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c296e-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c296e-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c296e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c296e-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c296e-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c296e-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c296e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c296e-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c296e-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c296e-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c296e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c296e-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c296e-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c296e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c296e-125">Requirements</span></span>



| <span data-ttu-id="c296e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c296e-126">Requirement</span></span> | <span data-ttu-id="c296e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c296e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c296e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c296e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c296e-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c296e-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c296e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c296e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c296e-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c296e-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c296e-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c296e-132">End of client support</span></span><br/>    | <span data-ttu-id="c296e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c296e-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c296e-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="c296e-134">Product</span></span><br/>                  | <span data-ttu-id="c296e-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c296e-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c296e-136">Header</span><span class="sxs-lookup"><span data-stu-id="c296e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c296e-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c296e-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c296e-138">IID</span><span class="sxs-lookup"><span data-stu-id="c296e-138">IID</span></span><br/>                      | <span data-ttu-id="c296e-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="c296e-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c296e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c296e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c296e-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="c296e-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

