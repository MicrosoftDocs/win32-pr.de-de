---
title: Ivmvirtualpc removeconfigurationvalue-Methode (vpccominterfaces. h)
description: Entfernt den Wert der angegebenen Konfigurationseinstellung.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Removeconfigurationvalue-Methode Virtual PC
- Removeconfigurationvalue-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, removeconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859134"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="d5839-106">Ivmvirtualpc:: removeconfigurationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="d5839-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="d5839-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5839-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d5839-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d5839-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d5839-109">Entfernt den Wert der angegebenen Konfigurationseinstellung.</span><span class="sxs-lookup"><span data-stu-id="d5839-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5839-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5839-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="d5839-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5839-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5839-112">*preferecekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5839-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5839-113">Der Schlüssel, der verwendet wird, um die Einstellung zu identifizieren, wie Sie in der Konfigurationsdatei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d5839-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5839-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5839-114">Return value</span></span>

<span data-ttu-id="d5839-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d5839-115">This method can return one of these values.</span></span>



| <span data-ttu-id="d5839-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d5839-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="d5839-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5839-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5839-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="d5839-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5839-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d5839-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="d5839-121">Der *preferecekey* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d5839-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="d5839-122"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="d5839-123">Der *preferencekey* -Parameter ist ungültig oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d5839-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="d5839-124"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="d5839-125">Die Einstellung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d5839-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d5839-126"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="d5839-127">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="d5839-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="d5839-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="d5839-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d5839-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d5839-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5839-130">Remarks</span></span>

<span data-ttu-id="d5839-131">Diese Methode ermöglicht den Zugriff auf niedriger Ebene auf einen beliebigen bevorzugten Wert für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d5839-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="d5839-132">Sie kann verwendet werden, um bevorzugte Werte für Kunden definierte Schlüssel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d5839-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5839-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5839-133">Requirements</span></span>



| <span data-ttu-id="d5839-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5839-134">Requirement</span></span> | <span data-ttu-id="d5839-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d5839-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5839-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5839-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d5839-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5839-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5839-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5839-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d5839-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5839-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d5839-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d5839-140">End of client support</span></span><br/>    | <span data-ttu-id="d5839-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5839-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d5839-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="d5839-142">Product</span></span><br/>                  | <span data-ttu-id="d5839-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d5839-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d5839-144">Header</span><span class="sxs-lookup"><span data-stu-id="d5839-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5839-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5839-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d5839-146">IID</span><span class="sxs-lookup"><span data-stu-id="d5839-146">IID</span></span><br/>                      | <span data-ttu-id="d5839-147">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="d5839-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d5839-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5839-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5839-149">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="d5839-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

