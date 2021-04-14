---
title: Ivmusbdevice-Eigenschaft deviceclass (vpccominterfaces. h)
description: Ruft die Geräteklasse des USB-Geräts ab.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- Eigenschaften von "tviceclass" (virtueller PC)
- Eigenschaften von "tviceclass" Virtual PC, ivmusbdevice-Schnittstelle
- Ivmusbdevice Interface Virtual PC, Eigenschaft "endviceclass"
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392103"
---
# <a name="ivmusbdevicedeviceclass-property"></a><span data-ttu-id="a818d-106">Ivmusbdevice::D eviceclass-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a818d-106">IVMUSBDevice::DeviceClass property</span></span>

<span data-ttu-id="a818d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a818d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a818d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a818d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a818d-109">Ruft die Geräteklasse des USB-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="a818d-109">Retrieves the device class of the USB device.</span></span>

<span data-ttu-id="a818d-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a818d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a818d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a818d-111">Syntax</span></span>


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a><span data-ttu-id="a818d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a818d-112">Property value</span></span>

<span data-ttu-id="a818d-113">Die Geräteklasse.</span><span class="sxs-lookup"><span data-stu-id="a818d-113">The device class.</span></span> <span data-ttu-id="a818d-114">Eine Liste der Werte finden Sie unter [**vmusbdebug-ID**](vmusbdeviceclassenum.md).</span><span class="sxs-lookup"><span data-stu-id="a818d-114">For a list of values, see [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="a818d-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a818d-115">Error codes</span></span>



| <span data-ttu-id="a818d-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a818d-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="a818d-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a818d-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="a818d-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a818d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="a818d-119">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a818d-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a818d-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a818d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="a818d-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a818d-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="a818d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a818d-122">Requirements</span></span>



| <span data-ttu-id="a818d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a818d-123">Requirement</span></span> | <span data-ttu-id="a818d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a818d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a818d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a818d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a818d-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a818d-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a818d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a818d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a818d-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a818d-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a818d-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a818d-129">End of client support</span></span><br/>    | <span data-ttu-id="a818d-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a818d-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a818d-131">Produkt</span><span class="sxs-lookup"><span data-stu-id="a818d-131">Product</span></span><br/>                  | <span data-ttu-id="a818d-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a818d-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a818d-133">Header</span><span class="sxs-lookup"><span data-stu-id="a818d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a818d-134"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a818d-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a818d-135">IID</span><span class="sxs-lookup"><span data-stu-id="a818d-135">IID</span></span><br/>                      | <span data-ttu-id="a818d-136">IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.</span><span class="sxs-lookup"><span data-stu-id="a818d-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a818d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a818d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a818d-138">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="a818d-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

