---
title: Ivmusbdevicecollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das USB-Geräte Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmusbdebug ecollection-Schnittstelle
- Ivmusbdebug-Schnittstelle virtueller PC, Element Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477046"
---
# <a name="ivmusbdevicecollectionitem-property"></a><span data-ttu-id="1789c-106">Ivmusbdebug:: Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1789c-106">IVMUSBDeviceCollection::Item property</span></span>

<span data-ttu-id="1789c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1789c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1789c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1789c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1789c-109">Ruft das USB-Geräte Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="1789c-109">Retrieves the USB device object that corresponds to the specified index.</span></span>

<span data-ttu-id="1789c-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1789c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1789c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1789c-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a><span data-ttu-id="1789c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1789c-112">Property value</span></span>

<span data-ttu-id="1789c-113">Das [**ivmusbdevice**](ivmusbdevice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1789c-113">The [**IVMUSBDevice**](ivmusbdevice.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1789c-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1789c-114">Error codes</span></span>



| <span data-ttu-id="1789c-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="1789c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1789c-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1789c-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1789c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1789c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1789c-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1789c-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="1789c-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1789c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1789c-120">Der *Parameter* "" ist **null**.</span><span class="sxs-lookup"><span data-stu-id="1789c-120">The *usbDevice* parameter is **NULL**.</span></span> <br/>                                             |
| <dl> <span data-ttu-id="1789c-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="1789c-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="1789c-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1789c-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="1789c-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1789c-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1789c-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1789c-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="1789c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1789c-125">Requirements</span></span>



| <span data-ttu-id="1789c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1789c-126">Requirement</span></span> | <span data-ttu-id="1789c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1789c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1789c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1789c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1789c-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1789c-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1789c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1789c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1789c-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1789c-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1789c-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1789c-132">End of client support</span></span><br/>    | <span data-ttu-id="1789c-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1789c-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1789c-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="1789c-134">Product</span></span><br/>                  | <span data-ttu-id="1789c-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1789c-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1789c-136">Header</span><span class="sxs-lookup"><span data-stu-id="1789c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1789c-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1789c-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1789c-138">IID</span><span class="sxs-lookup"><span data-stu-id="1789c-138">IID</span></span><br/>                      | <span data-ttu-id="1789c-139">IID \_ ivmusbdevicecollection ist als 4f-cd6a5--ID definiert. d1c-9s4d-e90abb8b3749</span><span class="sxs-lookup"><span data-stu-id="1789c-139">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="1789c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1789c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1789c-141">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="1789c-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="1789c-142">**Ivmusbde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="1789c-142">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

