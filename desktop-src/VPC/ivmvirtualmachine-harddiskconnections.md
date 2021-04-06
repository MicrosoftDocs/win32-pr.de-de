---
title: Ivmvirtualmachine harddiskconnections-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von Festplatten Verbindungen ab.
ms.assetid: 167eb8af-bbc1-49a8-83fd-8d946b50530d
keywords:
- Harddiskconnections-Eigenschaft virtueller PC
- Harddiskconnections-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, harddiskconnections (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HardDiskConnections
- IVMVirtualMachine.get_HardDiskConnections
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4a409337dc6fb437a98fe002f6e0d5d4da44b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742048"
---
# <a name="ivmvirtualmachineharddiskconnections-property"></a><span data-ttu-id="40b8f-106">Ivmvirtualmachine:: harddiskconnections (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40b8f-106">IVMVirtualMachine::HardDiskConnections property</span></span>

<span data-ttu-id="40b8f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40b8f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40b8f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40b8f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40b8f-109">Ruft eine Aufzähl Bare Auflistung von Festplatten Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="40b8f-109">Retrieves an enumerable collection of hard disk connections.</span></span>

<span data-ttu-id="40b8f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40b8f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b8f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="40b8f-111">Syntax</span></span>


```C++
HRESULT get_HardDiskConnections(
  [out, retval] IVMHardDiskConnectionCollection **hardDiskConnectionCollection
);
```



## <a name="property-value"></a><span data-ttu-id="40b8f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="40b8f-112">Property value</span></span>

<span data-ttu-id="40b8f-113">Ein [**ivmharddiskconnectioncollection**](ivmharddiskconnectioncollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="40b8f-113">An [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40b8f-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="40b8f-114">Error codes</span></span>



| <span data-ttu-id="40b8f-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="40b8f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="40b8f-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="40b8f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="40b8f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40b8f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="40b8f-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="40b8f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="40b8f-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="40b8f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="40b8f-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="40b8f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="40b8f-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="40b8f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="40b8f-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="40b8f-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="40b8f-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="40b8f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="40b8f-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="40b8f-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="40b8f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40b8f-125">Requirements</span></span>



| <span data-ttu-id="40b8f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40b8f-126">Requirement</span></span> | <span data-ttu-id="40b8f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="40b8f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40b8f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40b8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="40b8f-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40b8f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40b8f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40b8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="40b8f-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="40b8f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40b8f-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="40b8f-132">End of client support</span></span><br/>    | <span data-ttu-id="40b8f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40b8f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40b8f-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="40b8f-134">Product</span></span><br/>                  | <span data-ttu-id="40b8f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40b8f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40b8f-136">Header</span><span class="sxs-lookup"><span data-stu-id="40b8f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="40b8f-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40b8f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40b8f-138">IID</span><span class="sxs-lookup"><span data-stu-id="40b8f-138">IID</span></span><br/>                      | <span data-ttu-id="40b8f-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="40b8f-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="40b8f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40b8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b8f-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="40b8f-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

