---
title: Ivmharddiskconnection busnumber-Eigenschaft (vpccominterfaces. h)
description: Ruft die Busnummer ab, an die das Laufwerks Bild angefügt wird.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- Busnumber-Eigenschaft virtueller PC
- Busnumber-Eigenschaft Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection-Schnittstelle Virtual PC, busnumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477991"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a><span data-ttu-id="e37b1-106">Ivmharddiskconnection:: busnumber (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e37b1-106">IVMHardDiskConnection::BusNumber property</span></span>

<span data-ttu-id="e37b1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e37b1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e37b1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e37b1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e37b1-109">Ruft die Busnummer ab, an die das Laufwerks Bild angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e37b1-109">Retrieves the bus number to which the drive image is attached.</span></span>

<span data-ttu-id="e37b1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e37b1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e37b1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e37b1-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="e37b1-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e37b1-112">Property value</span></span>

<span data-ttu-id="e37b1-113">Die Busnummer, die dieser Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="e37b1-113">The bus number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e37b1-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e37b1-114">Error codes</span></span>



| <span data-ttu-id="e37b1-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e37b1-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="e37b1-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e37b1-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e37b1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e37b1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="e37b1-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e37b1-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="e37b1-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e37b1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="e37b1-120">Der-Parameter ist **null** oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="e37b1-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="e37b1-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="e37b1-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="e37b1-122">Die aktuelle Konfiguration der virtuellen Maschine ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e37b1-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="e37b1-123"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="e37b1-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="e37b1-124">Der Busstandort für diese Verbindung wurde nicht ordnungsgemäß initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e37b1-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="e37b1-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e37b1-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="e37b1-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e37b1-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="e37b1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e37b1-127">Requirements</span></span>



| <span data-ttu-id="e37b1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e37b1-128">Requirement</span></span> | <span data-ttu-id="e37b1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e37b1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37b1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e37b1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e37b1-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e37b1-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e37b1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e37b1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e37b1-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e37b1-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e37b1-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e37b1-134">End of client support</span></span><br/>    | <span data-ttu-id="e37b1-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e37b1-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e37b1-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="e37b1-136">Product</span></span><br/>                  | <span data-ttu-id="e37b1-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e37b1-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e37b1-138">Header</span><span class="sxs-lookup"><span data-stu-id="e37b1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e37b1-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e37b1-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e37b1-140">IID</span><span class="sxs-lookup"><span data-stu-id="e37b1-140">IID</span></span><br/>                      | <span data-ttu-id="e37b1-141">IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.</span><span class="sxs-lookup"><span data-stu-id="e37b1-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="e37b1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e37b1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e37b1-143">**Ivmharddiskconnection**</span><span class="sxs-lookup"><span data-stu-id="e37b1-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

