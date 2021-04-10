---
title: Ivmvirtualpc getconfigurationvalue-Methode (vpccominterfaces. h)
description: Ruft den Wert der angegebenen Konfigurationseinstellung ab
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Getconfigurationvalue-Methode Virtual PC
- Getconfigurationvalue-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105200"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="a497c-106">Ivmvirtualpc:: getconfigurationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="a497c-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="a497c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a497c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a497c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a497c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a497c-109">Ruft den Wert der angegebenen Konfigurationseinstellung ab</span><span class="sxs-lookup"><span data-stu-id="a497c-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="a497c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a497c-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="a497c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a497c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a497c-112">*preferecekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a497c-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a497c-113">Der Schlüssel, der verwendet wird, um die Einstellung zu identifizieren, wie Sie in der Konfigurationsdatei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a497c-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="a497c-114">*preferumcevalue* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a497c-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a497c-115">Der bevorzugte Wert.</span><span class="sxs-lookup"><span data-stu-id="a497c-115">The preference value.</span></span> <span data-ttu-id="a497c-116">Dieser Parameter kann einer der folgenden **Variant** -Typen sein: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) oder **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="a497c-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a497c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a497c-117">Return value</span></span>

<span data-ttu-id="a497c-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a497c-118">This method can return one of these values.</span></span>



| <span data-ttu-id="a497c-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a497c-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="a497c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a497c-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a497c-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a497c-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a497c-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a497c-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a497c-123"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a497c-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a497c-124">Der *preferecekey* -Parameter oder der *preferendcevalue* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a497c-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="a497c-125"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="a497c-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="a497c-126">Die Einstellung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a497c-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a497c-127"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a497c-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a497c-128">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a497c-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="a497c-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a497c-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a497c-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a497c-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a497c-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a497c-131">Remarks</span></span>

<span data-ttu-id="a497c-132">Diese Methode ermöglicht den Zugriff auf niedriger Ebene auf einen beliebigen bevorzugten Wert für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a497c-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="a497c-133">Sie kann verwendet werden, um bevorzugte Werte für Kunden definierte Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a497c-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="a497c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a497c-134">Requirements</span></span>



| <span data-ttu-id="a497c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a497c-135">Requirement</span></span> | <span data-ttu-id="a497c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a497c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a497c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a497c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a497c-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a497c-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a497c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a497c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a497c-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a497c-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a497c-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a497c-141">End of client support</span></span><br/>    | <span data-ttu-id="a497c-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a497c-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a497c-143">Produkt</span><span class="sxs-lookup"><span data-stu-id="a497c-143">Product</span></span><br/>                  | <span data-ttu-id="a497c-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a497c-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a497c-145">Header</span><span class="sxs-lookup"><span data-stu-id="a497c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a497c-146"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a497c-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a497c-147">IID</span><span class="sxs-lookup"><span data-stu-id="a497c-147">IID</span></span><br/>                      | <span data-ttu-id="a497c-148">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="a497c-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a497c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a497c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a497c-150">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="a497c-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

