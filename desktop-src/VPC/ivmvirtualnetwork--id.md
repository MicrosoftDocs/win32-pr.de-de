---
title: Ivmvirtualnetwork-_ID Methode (vpccominterfaces. h)
description: Ruft den internen Bezeichner des virtuellen Netzwerks ab.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID-Methode Virtual PC
- _ID-Methode Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, _ID-Methode
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040907"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="70326-106">Ivmvirtualnetwork:: \_ ID-Methode</span><span class="sxs-lookup"><span data-stu-id="70326-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="70326-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="70326-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="70326-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="70326-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="70326-109">Ruft den internen Bezeichner des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="70326-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="70326-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="70326-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="70326-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="70326-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70326-112">*virtualnetworkid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="70326-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70326-113">Der Bezeichner des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="70326-113">The virtual network identifier.</span></span> <span data-ttu-id="70326-114">Der Bezeichner für das virtuelle Netzwerk Shared Networking (NAT) lautet 01010101010101010101010101010101.</span><span class="sxs-lookup"><span data-stu-id="70326-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70326-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70326-115">Return value</span></span>

<span data-ttu-id="70326-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="70326-116">This method can return one of these values.</span></span>



| <span data-ttu-id="70326-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="70326-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="70326-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70326-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="70326-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70326-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="70326-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="70326-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="70326-121"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="70326-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="70326-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="70326-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="70326-123"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="70326-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="70326-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="70326-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="70326-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70326-125">Remarks</span></span>

<span data-ttu-id="70326-126">Diese Eigenschaft kann nicht von Skriptsprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70326-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="70326-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70326-127">Requirements</span></span>



| <span data-ttu-id="70326-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70326-128">Requirement</span></span> | <span data-ttu-id="70326-129">Wert</span><span class="sxs-lookup"><span data-stu-id="70326-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70326-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70326-130">Minimum supported client</span></span><br/> | <span data-ttu-id="70326-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70326-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70326-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70326-132">Minimum supported server</span></span><br/> | <span data-ttu-id="70326-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="70326-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="70326-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="70326-134">End of client support</span></span><br/>    | <span data-ttu-id="70326-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70326-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="70326-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="70326-136">Product</span></span><br/>                  | <span data-ttu-id="70326-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="70326-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="70326-138">Header</span><span class="sxs-lookup"><span data-stu-id="70326-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="70326-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="70326-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="70326-140">IID</span><span class="sxs-lookup"><span data-stu-id="70326-140">IID</span></span><br/>                      | <span data-ttu-id="70326-141">IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.</span><span class="sxs-lookup"><span data-stu-id="70326-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="70326-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70326-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70326-143">**Ivmvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="70326-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

