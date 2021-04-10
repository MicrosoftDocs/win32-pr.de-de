---
title: Ivmkeyboard tybäuerciitext-Methode (vpccominterfaces. h)
description: Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- Tybäuerciitext-Methode virtueller PC
- Tybäuerciitext-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, tybäuerciitext-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104271"
---
# <a name="ivmkeyboardtypeasciitext-method"></a><span data-ttu-id="6e7cc-106">Ivmkeyboard:: tybäuerciitext-Methode</span><span class="sxs-lookup"><span data-stu-id="6e7cc-106">IVMKeyboard::TypeAsciiText method</span></span>

<span data-ttu-id="6e7cc-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6e7cc-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6e7cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6e7cc-109">Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-109">Simulates a series of ASCII keys being typed into the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7cc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e7cc-110">Syntax</span></span>


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a><span data-ttu-id="6e7cc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e7cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e7cc-112">*Text* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e7cc-112">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7cc-113">Die ASCII-Text Zeichenfolge, die in den virtuellen Computer eingegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-113">The ASCII text string to be typed inside the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e7cc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e7cc-114">Return value</span></span>

<span data-ttu-id="6e7cc-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6e7cc-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6e7cc-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="6e7cc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e7cc-117">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6e7cc-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e7cc-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6e7cc-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="6e7cc-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6e7cc-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6e7cc-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="6e7cc-122"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6e7cc-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="6e7cc-123">Die angegebene Zeichenfolge ist leer.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-123">The specified string is empty.</span></span><br/>    |
| <dl> <span data-ttu-id="6e7cc-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6e7cc-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6e7cc-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-125">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e7cc-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e7cc-126">Requirements</span></span>



| <span data-ttu-id="6e7cc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e7cc-127">Requirement</span></span> | <span data-ttu-id="6e7cc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6e7cc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7cc-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e7cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7cc-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e7cc-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e7cc-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e7cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7cc-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6e7cc-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6e7cc-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6e7cc-133">End of client support</span></span><br/>    | <span data-ttu-id="6e7cc-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e7cc-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6e7cc-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="6e7cc-135">Product</span></span><br/>                  | <span data-ttu-id="6e7cc-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6e7cc-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6e7cc-137">Header</span><span class="sxs-lookup"><span data-stu-id="6e7cc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7cc-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e7cc-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6e7cc-139">IID</span><span class="sxs-lookup"><span data-stu-id="6e7cc-139">IID</span></span><br/>                      | <span data-ttu-id="6e7cc-140">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6e7cc-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e7cc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7cc-142">**Ivmkeyboard**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

