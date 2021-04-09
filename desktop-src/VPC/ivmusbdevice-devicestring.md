---
title: Ivmusbdevice devicestring-Eigenschaft (vpccominterfaces. h)
description: Ruft den Namen des USB-Geräts ab.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Devicestring-Eigenschaft virtueller PC
- Devicestring-Eigenschaft Virtual PC, ivmusbdevice-Schnittstelle
- Ivmusbdevice Interface Virtual PC, devicestring (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858952"
---
# <a name="ivmusbdevicedevicestring-property"></a><span data-ttu-id="7fc0d-106">Ivmusbdevice::D Eigenschaft "evicestring"</span><span class="sxs-lookup"><span data-stu-id="7fc0d-106">IVMUSBDevice::DeviceString property</span></span>

<span data-ttu-id="7fc0d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7fc0d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7fc0d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7fc0d-109">Ruft den Namen des USB-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-109">Retrieves the name of the USB device.</span></span>

<span data-ttu-id="7fc0d-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc0d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fc0d-111">Syntax</span></span>


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a><span data-ttu-id="7fc0d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7fc0d-112">Property value</span></span>

<span data-ttu-id="7fc0d-113">Der Name des USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-113">The name of the USB device.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7fc0d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7fc0d-114">Error codes</span></span>



| <span data-ttu-id="7fc0d-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7fc0d-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="7fc0d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7fc0d-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="7fc0d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7fc0d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="7fc0d-118">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7fc0d-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7fc0d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="7fc0d-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="7fc0d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fc0d-121">Requirements</span></span>



| <span data-ttu-id="7fc0d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fc0d-122">Requirement</span></span> | <span data-ttu-id="7fc0d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7fc0d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc0d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fc0d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc0d-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fc0d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fc0d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fc0d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc0d-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fc0d-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7fc0d-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7fc0d-128">End of client support</span></span><br/>    | <span data-ttu-id="7fc0d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7fc0d-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7fc0d-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="7fc0d-130">Product</span></span><br/>                  | <span data-ttu-id="7fc0d-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7fc0d-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7fc0d-132">Header</span><span class="sxs-lookup"><span data-stu-id="7fc0d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc0d-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc0d-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7fc0d-134">IID</span><span class="sxs-lookup"><span data-stu-id="7fc0d-134">IID</span></span><br/>                      | <span data-ttu-id="7fc0d-135">IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7fc0d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fc0d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc0d-137">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="7fc0d-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

