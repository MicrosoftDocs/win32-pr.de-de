---
title: Ivmparallelport-_ID Methode (vpccominterfaces. h)
description: Ruft den internen Bezeichner des parallelen Ports ab.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID-Methode Virtual PC
- _ID-Methode Virtual PC, ivmparallelport-Schnittstelle
- Ivmparallelport Interface Virtual PC, _ID-Methode
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338519"
---
# <a name="ivmparallelport_id-method"></a><span data-ttu-id="db6ba-106">Ivmparallelport:: \_ ID-Methode</span><span class="sxs-lookup"><span data-stu-id="db6ba-106">IVMParallelPort::\_ID method</span></span>

<span data-ttu-id="db6ba-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db6ba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="db6ba-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="db6ba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="db6ba-109">Ruft den internen Bezeichner des parallelen Ports ab.</span><span class="sxs-lookup"><span data-stu-id="db6ba-109">Retrieves the internal identifier of the parallel port.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6ba-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6ba-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="db6ba-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="db6ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6ba-112">*portid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db6ba-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db6ba-113">Der parallele Port Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="db6ba-113">The parallel port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6ba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db6ba-114">Return value</span></span>

<span data-ttu-id="db6ba-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="db6ba-115">This method can return one of these values.</span></span>



| <span data-ttu-id="db6ba-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="db6ba-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="db6ba-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db6ba-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="db6ba-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="db6ba-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="db6ba-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="db6ba-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="db6ba-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="db6ba-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="db6ba-122"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="db6ba-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="db6ba-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="db6ba-124"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="db6ba-125">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="db6ba-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db6ba-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db6ba-126">Remarks</span></span>

<span data-ttu-id="db6ba-127">Diese Eigenschaft kann nicht von Skriptsprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db6ba-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6ba-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6ba-128">Requirements</span></span>



| <span data-ttu-id="db6ba-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6ba-129">Requirement</span></span> | <span data-ttu-id="db6ba-130">Wert</span><span class="sxs-lookup"><span data-stu-id="db6ba-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6ba-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db6ba-131">Minimum supported client</span></span><br/> | <span data-ttu-id="db6ba-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db6ba-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db6ba-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db6ba-133">Minimum supported server</span></span><br/> | <span data-ttu-id="db6ba-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db6ba-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="db6ba-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="db6ba-135">End of client support</span></span><br/>    | <span data-ttu-id="db6ba-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db6ba-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="db6ba-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="db6ba-137">Product</span></span><br/>                  | <span data-ttu-id="db6ba-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="db6ba-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="db6ba-139">Header</span><span class="sxs-lookup"><span data-stu-id="db6ba-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6ba-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="db6ba-141">IID</span><span class="sxs-lookup"><span data-stu-id="db6ba-141">IID</span></span><br/>                      | <span data-ttu-id="db6ba-142">IID \_ ivmparallelport ist als 097beecb-0a02-474b-abd6-298b22293fc6 definiert.</span><span class="sxs-lookup"><span data-stu-id="db6ba-142">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="db6ba-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6ba-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6ba-144">**Ivmparallelport**</span><span class="sxs-lookup"><span data-stu-id="db6ba-144">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

