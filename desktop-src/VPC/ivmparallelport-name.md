---
title: Ivmparallelport-Namenseigenschaft (vpccominterfaces. h)
description: Der Name des parallelen Anschlusses.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmparallelport-Schnittstelle
- Ivmparallelport Interface Virtual PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102803"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="d1073-106">Ivmparallelport:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d1073-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="d1073-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1073-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1073-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1073-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1073-109">Ruft den Namen des parallelen Ports ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d1073-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="d1073-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d1073-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1073-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1073-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="d1073-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d1073-112">Property value</span></span>

<span data-ttu-id="d1073-113">Legt den Namen des parallelen Anschlusses fest (z. b. "LPT1").</span><span class="sxs-lookup"><span data-stu-id="d1073-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1073-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d1073-114">Error codes</span></span>



| <span data-ttu-id="d1073-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="d1073-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d1073-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d1073-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1073-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1073-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d1073-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1073-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="d1073-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d1073-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d1073-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d1073-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d1073-121"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d1073-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="d1073-122">Der-Parameter verweist auf einen ungültigen parallelen Port.</span><span class="sxs-lookup"><span data-stu-id="d1073-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d1073-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d1073-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d1073-124">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d1073-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="d1073-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1073-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d1073-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d1073-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="d1073-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1073-127">Requirements</span></span>



| <span data-ttu-id="d1073-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1073-128">Requirement</span></span> | <span data-ttu-id="d1073-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d1073-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1073-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1073-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d1073-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1073-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1073-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1073-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d1073-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d1073-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1073-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d1073-134">End of client support</span></span><br/>    | <span data-ttu-id="d1073-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1073-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1073-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="d1073-136">Product</span></span><br/>                  | <span data-ttu-id="d1073-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1073-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1073-138">Header</span><span class="sxs-lookup"><span data-stu-id="d1073-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1073-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1073-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1073-140">IID</span><span class="sxs-lookup"><span data-stu-id="d1073-140">IID</span></span><br/>                      | <span data-ttu-id="d1073-141">IID \_ ivmparallelport ist als 097beecb-0a02-474b-abd6-298b22293fc6 definiert.</span><span class="sxs-lookup"><span data-stu-id="d1073-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d1073-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1073-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1073-143">**Ivmparallelport**</span><span class="sxs-lookup"><span data-stu-id="d1073-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

