---
title: Ivmvirtualmachine rdppipename-Eigenschaft (vpccominterfaces. h)
description: Ruft den Namen der RDP-Verbindungs Named Pipe ab, die für Videos und Eingaben verwendet werden.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- Rdppipename-Eigenschaft virtueller PC
- Rdppipename-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, rdppipename-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040043"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="2a5e5-106">Ivmvirtualmachine:: rdppipename-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a5e5-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="2a5e5-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2a5e5-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2a5e5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2a5e5-109">Ruft den Namen der RDP-Verbindungs Named Pipe ab, die für Videos und Eingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="2a5e5-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a5e5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a5e5-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="2a5e5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2a5e5-112">Property value</span></span>

<span data-ttu-id="2a5e5-113">Der Name der RDP-Verbindungs Named Pipe, die für Videos und Eingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a5e5-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2a5e5-114">Error codes</span></span>

<span data-ttu-id="2a5e5-115">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2a5e5-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="2a5e5-117">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="2a5e5-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="2a5e5-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2a5e5-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="2a5e5-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e5-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="2a5e5-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="2a5e5-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e5-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="2a5e5-122">Der rdppipename-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="2a5e5-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="2a5e5-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="2a5e5-124">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="2a5e5-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e5-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="2a5e5-126">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="2a5e5-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a5e5-127">Requirements</span></span>



| <span data-ttu-id="2a5e5-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a5e5-128">Requirement</span></span> | <span data-ttu-id="2a5e5-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2a5e5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5e5-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a5e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a5e5-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a5e5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a5e5-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a5e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a5e5-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2a5e5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a5e5-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2a5e5-134">End of client support</span></span><br/>    | <span data-ttu-id="2a5e5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a5e5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2a5e5-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="2a5e5-136">Product</span></span><br/>                  | <span data-ttu-id="2a5e5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2a5e5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2a5e5-138">Header</span><span class="sxs-lookup"><span data-stu-id="2a5e5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a5e5-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2a5e5-140">IID</span><span class="sxs-lookup"><span data-stu-id="2a5e5-140">IID</span></span><br/>                      | <span data-ttu-id="2a5e5-141">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="2a5e5-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2a5e5-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a5e5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a5e5-143">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="2a5e5-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

