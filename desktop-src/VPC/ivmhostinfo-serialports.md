---
title: Ivmhostinfo serialports-Eigenschaft (vpccominterfaces. h)
description: Ruft die seriellen Anschluss Namen ab, die den seriellen Ports des Hosts zugeordnet sind.
ms.assetid: ef3bc474-19c9-4d91-8aa0-7619c89fec2d
keywords:
- Serialports-Eigenschaft virtueller PC
- Serialports-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, SerialPorts (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.SerialPorts
- IVMHostInfo.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8cb520ee82b53e93f9073b66d4dc4d69a2ef75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040049"
---
# <a name="ivmhostinfoserialports-property"></a><span data-ttu-id="499f5-106">Ivmhostinfo:: serialports (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="499f5-106">IVMHostInfo::SerialPorts property</span></span>

<span data-ttu-id="499f5-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="499f5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="499f5-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="499f5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="499f5-109">Ruft die seriellen Anschluss Namen ab, die den seriellen Ports des Hosts zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="499f5-109">Retrieves the serial port names associated with host serial ports.</span></span>

<span data-ttu-id="499f5-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="499f5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="499f5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="499f5-111">Syntax</span></span>


```C++
HRESULT get_SerialPorts(
  [out, retval] BSTR *serialPorts
);
```



## <a name="property-value"></a><span data-ttu-id="499f5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="499f5-112">Property value</span></span>

<span data-ttu-id="499f5-113">Eine durch Semikolons getrennte Liste von seriellen Anschluss Namen.</span><span class="sxs-lookup"><span data-stu-id="499f5-113">A semicolon-delimited list of serial port names.</span></span>

## <a name="error-codes"></a><span data-ttu-id="499f5-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="499f5-114">Error codes</span></span>



| <span data-ttu-id="499f5-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="499f5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="499f5-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="499f5-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="499f5-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="499f5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="499f5-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="499f5-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="499f5-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="499f5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="499f5-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="499f5-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="499f5-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="499f5-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="499f5-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="499f5-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="499f5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="499f5-123">Requirements</span></span>



| <span data-ttu-id="499f5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="499f5-124">Requirement</span></span> | <span data-ttu-id="499f5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="499f5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="499f5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="499f5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="499f5-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="499f5-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="499f5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="499f5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="499f5-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="499f5-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="499f5-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="499f5-130">End of client support</span></span><br/>    | <span data-ttu-id="499f5-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="499f5-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="499f5-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="499f5-132">Product</span></span><br/>                  | <span data-ttu-id="499f5-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="499f5-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="499f5-134">Header</span><span class="sxs-lookup"><span data-stu-id="499f5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="499f5-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="499f5-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="499f5-136">IID</span><span class="sxs-lookup"><span data-stu-id="499f5-136">IID</span></span><br/>                      | <span data-ttu-id="499f5-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="499f5-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="499f5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="499f5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499f5-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="499f5-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

