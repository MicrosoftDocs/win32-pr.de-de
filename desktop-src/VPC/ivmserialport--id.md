---
title: Ivmserialport-_ID Methode (vpccominterfaces. h)
description: Interner Bezeichner des seriellen Anschlusses.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID-Methode Virtual PC
- _ID-Methode Virtual PC, ivmserialport-Schnittstelle
- Ivmserialport Interface Virtual PC, _ID-Methode
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103591"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="6324a-106">Ivmserialport:: \_ ID-Methode</span><span class="sxs-lookup"><span data-stu-id="6324a-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="6324a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6324a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6324a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6324a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6324a-109">Ruft den internen Bezeichner des seriellen Anschlusses ab.</span><span class="sxs-lookup"><span data-stu-id="6324a-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="6324a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6324a-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="6324a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6324a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6324a-112">*portid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6324a-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6324a-113">Der Bezeichner des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="6324a-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6324a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6324a-114">Return value</span></span>

<span data-ttu-id="6324a-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6324a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6324a-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6324a-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="6324a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6324a-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="6324a-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6324a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6324a-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6324a-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="6324a-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6324a-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6324a-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6324a-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="6324a-122"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6324a-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6324a-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6324a-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="6324a-124"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="6324a-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6324a-125">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6324a-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6324a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6324a-126">Remarks</span></span>

<span data-ttu-id="6324a-127">Diese Eigenschaft kann nicht von Skriptsprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6324a-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="6324a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6324a-128">Requirements</span></span>



| <span data-ttu-id="6324a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6324a-129">Requirement</span></span> | <span data-ttu-id="6324a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6324a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6324a-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6324a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6324a-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6324a-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6324a-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6324a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6324a-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6324a-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6324a-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6324a-135">End of client support</span></span><br/>    | <span data-ttu-id="6324a-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6324a-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6324a-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="6324a-137">Product</span></span><br/>                  | <span data-ttu-id="6324a-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6324a-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6324a-139">Header</span><span class="sxs-lookup"><span data-stu-id="6324a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6324a-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6324a-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6324a-141">IID</span><span class="sxs-lookup"><span data-stu-id="6324a-141">IID</span></span><br/>                      | <span data-ttu-id="6324a-142">IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.</span><span class="sxs-lookup"><span data-stu-id="6324a-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="6324a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6324a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6324a-144">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="6324a-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

