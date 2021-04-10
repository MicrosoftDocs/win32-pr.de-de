---
title: Ivmnetworkadapter isethernetaddressdynamic-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob die Ethernet-Adresse dynamisch generiert wird.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- Isethernetaddressdynamic-Eigenschaft virtueller PC
- Isethernetaddressdynamic-Eigenschaft Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, isethernetaddressdynamic (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040048"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="645e9-106">Ivmnetworkadapter:: isethernetaddressdynamic (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="645e9-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="645e9-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="645e9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="645e9-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="645e9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="645e9-109">Bestimmt, ob die Ethernet-Adresse dynamisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="645e9-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="645e9-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="645e9-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="645e9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="645e9-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="645e9-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="645e9-112">Property value</span></span>

<span data-ttu-id="645e9-113">Auf Variant true festgelegt, \_ Wenn die Ethernet-Adresse dynamisch generiert werden soll, und Variant \_ false, wenn die Ethernet-Adresse statisch ist.</span><span class="sxs-lookup"><span data-stu-id="645e9-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="645e9-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="645e9-114">Error codes</span></span>



| <span data-ttu-id="645e9-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="645e9-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="645e9-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="645e9-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="645e9-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="645e9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="645e9-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="645e9-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="645e9-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="645e9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="645e9-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="645e9-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="645e9-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="645e9-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="645e9-122">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="645e9-122">The virtual machine was not found.</span></span> <span data-ttu-id="645e9-123">Dies kann vorkommen, wenn der Computer entfernt wurde, nachdem das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="645e9-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="645e9-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="645e9-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="645e9-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="645e9-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="645e9-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="645e9-126">Remarks</span></span>

<span data-ttu-id="645e9-127">Diese Eigenschaft sollte für die meisten virtuellen Netzwerkschnittstellen auf **true** (Standardeinstellung) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="645e9-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="645e9-128">Wenn für die Software im Gast eine statische Ethernet-Adresse erforderlich ist, sollte diese Eigenschaft auf " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="645e9-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="645e9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="645e9-129">Requirements</span></span>



| <span data-ttu-id="645e9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="645e9-130">Requirement</span></span> | <span data-ttu-id="645e9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="645e9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="645e9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="645e9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="645e9-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="645e9-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="645e9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="645e9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="645e9-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="645e9-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="645e9-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="645e9-136">End of client support</span></span><br/>    | <span data-ttu-id="645e9-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="645e9-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="645e9-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="645e9-138">Product</span></span><br/>                  | <span data-ttu-id="645e9-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="645e9-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="645e9-140">Header</span><span class="sxs-lookup"><span data-stu-id="645e9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="645e9-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="645e9-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="645e9-142">IID</span><span class="sxs-lookup"><span data-stu-id="645e9-142">IID</span></span><br/>                      | <span data-ttu-id="645e9-143">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="645e9-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="645e9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="645e9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645e9-145">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="645e9-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

