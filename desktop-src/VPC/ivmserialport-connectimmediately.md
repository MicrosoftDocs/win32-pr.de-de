---
title: Ivmserialport connectimmediately-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Connectimmediately-Eigenschaft virtueller PC
- Connectimmediately-Eigenschaft Virtual PC, ivmserialport-Schnittstelle
- Ivmserialport Interface Virtual PC, connectimmediately (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741744"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="bca18-106">Ivmserialport:: connectimmediately (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bca18-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="bca18-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bca18-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bca18-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bca18-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bca18-109">Bestimmt, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="bca18-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="bca18-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bca18-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca18-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bca18-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="bca18-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bca18-112">Property value</span></span>

<span data-ttu-id="bca18-113">**Variant \_ TRUE** , wenn der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird. **Variant \_ Andernfalls false** .</span><span class="sxs-lookup"><span data-stu-id="bca18-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bca18-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bca18-114">Error codes</span></span>



| <span data-ttu-id="bca18-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="bca18-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bca18-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bca18-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="bca18-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bca18-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bca18-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bca18-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="bca18-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bca18-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bca18-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bca18-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="bca18-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="bca18-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="bca18-122">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bca18-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="bca18-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bca18-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bca18-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bca18-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="bca18-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bca18-125">Remarks</span></span>

<span data-ttu-id="bca18-126">Diese Eigenschaft ist nur gültig, wenn die [**Porttyp**](ivmserialport-type.md) -Eigenschaft **vmserialport \_ hostport** ist.</span><span class="sxs-lookup"><span data-stu-id="bca18-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bca18-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bca18-127">Requirements</span></span>



| <span data-ttu-id="bca18-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bca18-128">Requirement</span></span> | <span data-ttu-id="bca18-129">Wert</span><span class="sxs-lookup"><span data-stu-id="bca18-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca18-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bca18-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bca18-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bca18-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bca18-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bca18-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bca18-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bca18-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bca18-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bca18-134">End of client support</span></span><br/>    | <span data-ttu-id="bca18-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bca18-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bca18-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="bca18-136">Product</span></span><br/>                  | <span data-ttu-id="bca18-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bca18-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bca18-138">Header</span><span class="sxs-lookup"><span data-stu-id="bca18-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bca18-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bca18-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bca18-140">IID</span><span class="sxs-lookup"><span data-stu-id="bca18-140">IID</span></span><br/>                      | <span data-ttu-id="bca18-141">IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.</span><span class="sxs-lookup"><span data-stu-id="bca18-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="bca18-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bca18-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca18-143">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="bca18-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

