---
title: Ivmusbdevice hubid-Eigenschaft (vpccominterfaces. h)
description: Ruft den Bezeichner des Hubs ab, mit dem das Gerät verbunden ist.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- Hubid-Eigenschaft virtueller PC
- Hubid-Eigenschaft Virtual PC, ivmusbdevice-Schnittstelle
- Ivmusbdevice Interface Virtual PC, hubid (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53faa79ee999022f993070767846ee4e4723c3a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040816"
---
# <a name="ivmusbdevicehubid-property"></a><span data-ttu-id="e097f-106">Ivmusbdevice:: hubid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e097f-106">IVMUSBDevice::HubID property</span></span>

<span data-ttu-id="e097f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e097f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e097f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e097f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e097f-109">Ruft den Bezeichner des Hubs ab, mit dem das Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e097f-109">Retrieves the identifier of the hub on which the device is connected.</span></span>

<span data-ttu-id="e097f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e097f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e097f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e097f-111">Syntax</span></span>


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a><span data-ttu-id="e097f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e097f-112">Property value</span></span>

<span data-ttu-id="e097f-113">Der Hub-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e097f-113">The hub identifier.</span></span> <span data-ttu-id="e097f-114">Dieser Wert wird vom USB-Connector-Treiber zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e097f-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e097f-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e097f-115">Error codes</span></span>



| <span data-ttu-id="e097f-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e097f-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="e097f-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e097f-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e097f-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e097f-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="e097f-119">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e097f-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e097f-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e097f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="e097f-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e097f-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="e097f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e097f-122">Requirements</span></span>



| <span data-ttu-id="e097f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e097f-123">Requirement</span></span> | <span data-ttu-id="e097f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e097f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e097f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e097f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e097f-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e097f-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e097f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e097f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e097f-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e097f-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e097f-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e097f-129">End of client support</span></span><br/>    | <span data-ttu-id="e097f-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e097f-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e097f-131">Produkt</span><span class="sxs-lookup"><span data-stu-id="e097f-131">Product</span></span><br/>                  | <span data-ttu-id="e097f-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e097f-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e097f-133">Header</span><span class="sxs-lookup"><span data-stu-id="e097f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e097f-134"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e097f-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e097f-135">IID</span><span class="sxs-lookup"><span data-stu-id="e097f-135">IID</span></span><br/>                      | <span data-ttu-id="e097f-136">IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.</span><span class="sxs-lookup"><span data-stu-id="e097f-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e097f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e097f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e097f-138">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="e097f-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

