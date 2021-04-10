---
title: Ivmkeyboard releasekey-Methode (vpccominterfaces. h)
description: Simuliert einen Schlüssel, der freigegeben wird.
ms.assetid: 112bf11d-d768-4487-ab41-e915aa4e6a24
keywords:
- Releasekey-Methode Virtual PC
- Releasekey-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, releasekey-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.ReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8585f592ae1cad65157536f841500c42bb06bfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956660"
---
# <a name="ivmkeyboardreleasekey-method"></a><span data-ttu-id="b9546-106">Ivmkeyboard:: releasekey-Methode</span><span class="sxs-lookup"><span data-stu-id="b9546-106">IVMKeyboard::ReleaseKey method</span></span>

<span data-ttu-id="b9546-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9546-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b9546-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b9546-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b9546-109">Simuliert einen Schlüssel, der freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b9546-109">Simulates a key being released.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9546-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9546-110">Syntax</span></span>


```C++
HRESULT ReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="b9546-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9546-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9546-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9546-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9546-113">Der Schlüsselcode für den Schlüssel, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9546-113">The key code for the key to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9546-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9546-114">Return value</span></span>

<span data-ttu-id="b9546-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b9546-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b9546-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b9546-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="b9546-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9546-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9546-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9546-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b9546-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9546-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b9546-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b9546-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b9546-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b9546-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b9546-122"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b9546-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="b9546-123">Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.</span><span class="sxs-lookup"><span data-stu-id="b9546-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="b9546-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b9546-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b9546-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b9546-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="b9546-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9546-126">Requirements</span></span>



| <span data-ttu-id="b9546-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9546-127">Requirement</span></span> | <span data-ttu-id="b9546-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b9546-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9546-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9546-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9546-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9546-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9546-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9546-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9546-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9546-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b9546-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b9546-133">End of client support</span></span><br/>    | <span data-ttu-id="b9546-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9546-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b9546-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="b9546-135">Product</span></span><br/>                  | <span data-ttu-id="b9546-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b9546-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b9546-137">Header</span><span class="sxs-lookup"><span data-stu-id="b9546-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9546-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9546-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b9546-139">IID</span><span class="sxs-lookup"><span data-stu-id="b9546-139">IID</span></span><br/>                      | <span data-ttu-id="b9546-140">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="b9546-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b9546-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9546-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9546-142">**Ivmkeyboard**</span><span class="sxs-lookup"><span data-stu-id="b9546-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

