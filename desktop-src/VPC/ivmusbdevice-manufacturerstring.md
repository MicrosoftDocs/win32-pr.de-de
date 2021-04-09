---
title: Ivmusbdevice manufacturerstring-Eigenschaft (vpccominterfaces. h)
description: Ruft den Namen des USB-Geräteherstellers ab.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Manufacturerstring-Eigenschaft virtueller PC
- Manufacturerstring-Eigenschaft Virtual PC, ivmusbdevice-Schnittstelle
- Ivmusbdevice Interface Virtual PC, manufacturerstring (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8d74cbe737c59e10daf2cf3ee93e4b1f14983f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104912"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a><span data-ttu-id="095f4-106">Ivmusbdevice:: manufacturerstring (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="095f4-106">IVMUSBDevice::ManufacturerString property</span></span>

<span data-ttu-id="095f4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="095f4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="095f4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="095f4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="095f4-109">Ruft den Namen des USB-Geräteherstellers ab.</span><span class="sxs-lookup"><span data-stu-id="095f4-109">Retrieves the name of the USB device manufacturer.</span></span>

<span data-ttu-id="095f4-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="095f4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="095f4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="095f4-111">Syntax</span></span>


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a><span data-ttu-id="095f4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="095f4-112">Property value</span></span>

<span data-ttu-id="095f4-113">Der Name des Herstellers des USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="095f4-113">The name of the USB device manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="095f4-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="095f4-114">Error codes</span></span>



| <span data-ttu-id="095f4-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="095f4-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="095f4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="095f4-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="095f4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="095f4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="095f4-118">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="095f4-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="095f4-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="095f4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="095f4-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="095f4-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="095f4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="095f4-121">Requirements</span></span>



| <span data-ttu-id="095f4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="095f4-122">Requirement</span></span> | <span data-ttu-id="095f4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="095f4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="095f4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="095f4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="095f4-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="095f4-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="095f4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="095f4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="095f4-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="095f4-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="095f4-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="095f4-128">End of client support</span></span><br/>    | <span data-ttu-id="095f4-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="095f4-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="095f4-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="095f4-130">Product</span></span><br/>                  | <span data-ttu-id="095f4-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="095f4-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="095f4-132">Header</span><span class="sxs-lookup"><span data-stu-id="095f4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="095f4-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="095f4-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="095f4-134">IID</span><span class="sxs-lookup"><span data-stu-id="095f4-134">IID</span></span><br/>                      | <span data-ttu-id="095f4-135">IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.</span><span class="sxs-lookup"><span data-stu-id="095f4-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="095f4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="095f4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095f4-137">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="095f4-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

