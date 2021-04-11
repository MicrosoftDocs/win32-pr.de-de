---
title: Ivmharddiskconnection devicenenumber-Eigenschaft (vpccominterfaces. h)
description: Ruft die Gerätenummer ab, an die das Laufwerks Image angefügt wird.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- Devicenenber-Eigenschaft virtueller PC
- Devicenenber-Eigenschaft Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection Interface Virtual PC, devicenumschlag-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105807"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a><span data-ttu-id="075b7-106">Ivmharddiskconnection::D-Eigenschaft ' evicenenber '</span><span class="sxs-lookup"><span data-stu-id="075b7-106">IVMHardDiskConnection::DeviceNumber property</span></span>

<span data-ttu-id="075b7-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="075b7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="075b7-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="075b7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="075b7-109">Ruft die Gerätenummer ab, an die das Laufwerks Image angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="075b7-109">Retrieves the device number to which the drive image is attached.</span></span>

<span data-ttu-id="075b7-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="075b7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="075b7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="075b7-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="075b7-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="075b7-112">Property value</span></span>

<span data-ttu-id="075b7-113">Die Gerätenummer, die dieser Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="075b7-113">The device number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="075b7-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="075b7-114">Error codes</span></span>



| <span data-ttu-id="075b7-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="075b7-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="075b7-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="075b7-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="075b7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="075b7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="075b7-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="075b7-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="075b7-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="075b7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="075b7-120">Der-Parameter ist **null** oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="075b7-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="075b7-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="075b7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="075b7-122">Die aktuelle Konfiguration der virtuellen Maschine ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="075b7-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="075b7-123"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="075b7-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="075b7-124">Der Busstandort für diese Verbindung wurde nicht ordnungsgemäß initialisiert.</span><span class="sxs-lookup"><span data-stu-id="075b7-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="075b7-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="075b7-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="075b7-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="075b7-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="075b7-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="075b7-127">Requirements</span></span>



| <span data-ttu-id="075b7-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="075b7-128">Requirement</span></span> | <span data-ttu-id="075b7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="075b7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="075b7-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="075b7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="075b7-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="075b7-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="075b7-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="075b7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="075b7-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="075b7-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="075b7-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="075b7-134">End of client support</span></span><br/>    | <span data-ttu-id="075b7-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="075b7-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="075b7-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="075b7-136">Product</span></span><br/>                  | <span data-ttu-id="075b7-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="075b7-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="075b7-138">Header</span><span class="sxs-lookup"><span data-stu-id="075b7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="075b7-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="075b7-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="075b7-140">IID</span><span class="sxs-lookup"><span data-stu-id="075b7-140">IID</span></span><br/>                      | <span data-ttu-id="075b7-141">IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.</span><span class="sxs-lookup"><span data-stu-id="075b7-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="075b7-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="075b7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075b7-143">**Ivmharddiskconnection**</span><span class="sxs-lookup"><span data-stu-id="075b7-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

