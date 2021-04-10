---
title: Ivmnetworkadapter-_ID Methode (vpccominterfaces. h)
description: Ruft den internen Bezeichner dieser Netzwerkschnittstelle ab.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID-Methode Virtual PC
- _ID-Methode Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, _ID-Methode
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956593"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="d89e1-106">Ivmnetworkadapter:: \_ ID-Methode</span><span class="sxs-lookup"><span data-stu-id="d89e1-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="d89e1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d89e1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d89e1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d89e1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d89e1-109">Ruft den internen Bezeichner dieser Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="d89e1-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89e1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d89e1-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="d89e1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d89e1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d89e1-112">*Bezeichner* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d89e1-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89e1-113">Der interne Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d89e1-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d89e1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d89e1-114">Return value</span></span>

<span data-ttu-id="d89e1-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d89e1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="d89e1-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d89e1-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="d89e1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d89e1-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="d89e1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d89e1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d89e1-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d89e1-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="d89e1-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d89e1-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d89e1-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d89e1-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="d89e1-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d89e1-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d89e1-123">Der virtuelle Computer kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d89e1-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="d89e1-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d89e1-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d89e1-125">Unbekannter Fehler beim Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d89e1-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d89e1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d89e1-126">Remarks</span></span>

<span data-ttu-id="d89e1-127">Diese Methode kann nicht von Skriptsprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d89e1-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="d89e1-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d89e1-128">Requirements</span></span>



| <span data-ttu-id="d89e1-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d89e1-129">Requirement</span></span> | <span data-ttu-id="d89e1-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d89e1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89e1-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d89e1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d89e1-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d89e1-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d89e1-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d89e1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d89e1-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d89e1-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d89e1-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d89e1-135">End of client support</span></span><br/>    | <span data-ttu-id="d89e1-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d89e1-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d89e1-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="d89e1-137">Product</span></span><br/>                  | <span data-ttu-id="d89e1-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d89e1-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d89e1-139">Header</span><span class="sxs-lookup"><span data-stu-id="d89e1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d89e1-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89e1-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d89e1-141">IID</span><span class="sxs-lookup"><span data-stu-id="d89e1-141">IID</span></span><br/>                      | <span data-ttu-id="d89e1-142">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="d89e1-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d89e1-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d89e1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89e1-144">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="d89e1-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

