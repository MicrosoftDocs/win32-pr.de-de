---
title: Ivmusbdevice-Port Eigenschaft (vpccominterfaces. h)
description: Ruft den Bezeichner des Ports ab, mit dem das Gerät verbunden ist.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Port Eigenschaft virtueller PC
- Port Eigenschaft Virtual PC, ivmusbdevice-Schnittstelle
- Ivmusbdevice Interface Virtual PC, Port (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743240"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="f35f3-106">Ivmusbdevice::P Ort (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f35f3-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="f35f3-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f35f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f35f3-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f35f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f35f3-109">Ruft den Bezeichner des Ports ab, mit dem das Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f35f3-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="f35f3-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f35f3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35f3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f35f3-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="f35f3-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f35f3-112">Property value</span></span>

<span data-ttu-id="f35f3-113">Der Port Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f35f3-113">The port identifier.</span></span> <span data-ttu-id="f35f3-114">Dieser Wert wird vom USB-Connector-Treiber zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f35f3-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f35f3-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f35f3-115">Error codes</span></span>



| <span data-ttu-id="f35f3-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="f35f3-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="f35f3-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f35f3-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f35f3-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f35f3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="f35f3-119">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f35f3-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f35f3-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f35f3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="f35f3-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f35f3-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="f35f3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f35f3-122">Requirements</span></span>



| <span data-ttu-id="f35f3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f35f3-123">Requirement</span></span> | <span data-ttu-id="f35f3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f35f3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f35f3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f35f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f35f3-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f35f3-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f35f3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f35f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f35f3-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f35f3-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f35f3-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f35f3-129">End of client support</span></span><br/>    | <span data-ttu-id="f35f3-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f35f3-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f35f3-131">Produkt</span><span class="sxs-lookup"><span data-stu-id="f35f3-131">Product</span></span><br/>                  | <span data-ttu-id="f35f3-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f35f3-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f35f3-133">Header</span><span class="sxs-lookup"><span data-stu-id="f35f3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f35f3-134"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f35f3-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f35f3-135">IID</span><span class="sxs-lookup"><span data-stu-id="f35f3-135">IID</span></span><br/>                      | <span data-ttu-id="f35f3-136">IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.</span><span class="sxs-lookup"><span data-stu-id="f35f3-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f35f3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f35f3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35f3-138">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="f35f3-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

