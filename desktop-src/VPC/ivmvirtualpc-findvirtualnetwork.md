---
title: Ivmvirtualpc findvirtualnetwork-Methode (vpccominterfaces. h)
description: Ruft ein virtuelles Netzwerk Objekt ab, das mit dem angeforderten Namen übereinstimmt.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Findvirtualnetwork-Methode Virtual PC
- Findvirtualnetwork-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, findvirtualnetwork-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518470"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="c145a-106">Ivmvirtualpc:: findvirtualnetwork-Methode</span><span class="sxs-lookup"><span data-stu-id="c145a-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="c145a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c145a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c145a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c145a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c145a-109">Ruft ein virtuelles Netzwerk Objekt ab, das mit dem angeforderten Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c145a-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c145a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c145a-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="c145a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c145a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c145a-112">*virtualnetworkname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c145a-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c145a-113">Der Name des zu suchenden virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="c145a-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="c145a-114">*VirtualNetwork* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c145a-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c145a-115">Ein Zeiger auf ein neues [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt, das dieses virtuelle Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="c145a-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c145a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c145a-116">Return value</span></span>

<span data-ttu-id="c145a-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c145a-117">This method can return one of these values.</span></span>



| <span data-ttu-id="c145a-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c145a-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="c145a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c145a-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c145a-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="c145a-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c145a-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c145a-122"><dt>**S \_ Falsch**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="c145a-123">Das angegebene virtuelle Netzwerk konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c145a-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c145a-124"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="c145a-125">Der *VirtualNetwork* -Parameter ist **null** , oder das virtuelle Netzwerk kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c145a-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="c145a-126"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="c145a-127">Der Parameter " *virtualnetworkname* " ist ungültig oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c145a-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="c145a-128"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="c145a-129">Die virtuelle Netzwerkdatei konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c145a-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="c145a-130"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="c145a-131">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c145a-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="c145a-132"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="c145a-133">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="c145a-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c145a-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c145a-134">Remarks</span></span>

<span data-ttu-id="c145a-135">Bei Namen von virtuellen Netzwerken wird die Groß-/Kleinschreibung nicht beachtet, z. b. "mynetwork" und "mynetwork" beziehen sich auf dasselbe virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c145a-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="c145a-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c145a-136">Requirements</span></span>



| <span data-ttu-id="c145a-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c145a-137">Requirement</span></span> | <span data-ttu-id="c145a-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c145a-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c145a-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c145a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c145a-140">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c145a-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c145a-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c145a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c145a-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c145a-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c145a-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c145a-143">End of client support</span></span><br/>    | <span data-ttu-id="c145a-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c145a-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c145a-145">Produkt</span><span class="sxs-lookup"><span data-stu-id="c145a-145">Product</span></span><br/>                  | <span data-ttu-id="c145a-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c145a-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c145a-147">Header</span><span class="sxs-lookup"><span data-stu-id="c145a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="c145a-148"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c145a-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c145a-149">IID</span><span class="sxs-lookup"><span data-stu-id="c145a-149">IID</span></span><br/>                      | <span data-ttu-id="c145a-150">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="c145a-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c145a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c145a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c145a-152">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="c145a-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

