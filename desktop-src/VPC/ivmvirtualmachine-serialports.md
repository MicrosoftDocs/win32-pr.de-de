---
title: Ivmvirtualmachine serialports-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von seriellen Anschlüssen ab.
ms.assetid: 502fe4f1-c58c-460c-8431-41fddd753d18
keywords:
- Serialports-Eigenschaft virtueller PC
- Serialports-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, SerialPorts (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SerialPorts
- IVMVirtualMachine.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18119c649014a020dd2a2d4e2fdeb7c2bbaae87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518575"
---
# <a name="ivmvirtualmachineserialports-property"></a><span data-ttu-id="c0ce8-106">Ivmvirtualmachine:: serialports (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0ce8-106">IVMVirtualMachine::SerialPorts property</span></span>

<span data-ttu-id="c0ce8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0ce8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0ce8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0ce8-109">Ruft eine Aufzähl Bare Auflistung von seriellen Anschlüssen ab.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-109">Retrieves an enumerable collection of serial ports.</span></span>

<span data-ttu-id="c0ce8-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ce8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0ce8-111">Syntax</span></span>


```C++
HRESULT get_SerialPorts(
  [out, retval] IVMSerialPortCollection **serialPortCollection
);
```



## <a name="property-value"></a><span data-ttu-id="c0ce8-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c0ce8-112">Property value</span></span>

<span data-ttu-id="c0ce8-113">Ein [**ivmserialportcollection**](ivmserialportcollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-113">An [**IVMSerialPortCollection**](ivmserialportcollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0ce8-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c0ce8-114">Error codes</span></span>



| <span data-ttu-id="c0ce8-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c0ce8-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c0ce8-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c0ce8-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c0ce8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c0ce8-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c0ce8-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c0ce8-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c0ce8-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce8-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c0ce8-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c0ce8-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce8-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c0ce8-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c0ce8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0ce8-125">Requirements</span></span>



| <span data-ttu-id="c0ce8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0ce8-126">Requirement</span></span> | <span data-ttu-id="c0ce8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ce8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ce8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0ce8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ce8-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0ce8-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0ce8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0ce8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ce8-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0ce8-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0ce8-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c0ce8-132">End of client support</span></span><br/>    | <span data-ttu-id="c0ce8-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0ce8-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0ce8-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="c0ce8-134">Product</span></span><br/>                  | <span data-ttu-id="c0ce8-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0ce8-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0ce8-136">Header</span><span class="sxs-lookup"><span data-stu-id="c0ce8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ce8-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce8-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0ce8-138">IID</span><span class="sxs-lookup"><span data-stu-id="c0ce8-138">IID</span></span><br/>                      | <span data-ttu-id="c0ce8-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c0ce8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0ce8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ce8-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="c0ce8-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

