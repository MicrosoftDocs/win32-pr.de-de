---
title: Ivmkeyboard pressandreleasekey-Methode (vpccominterfaces. h)
description: Simuliert, dass eine Taste gedrückt und anschließend freigegeben wird.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Pressandreleasekey-Methode Virtual PC
- Pressandreleasekey-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, pressandreleasekey-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339163"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="086c7-106">Ivmkeyboard::P ressandreleasekey-Methode</span><span class="sxs-lookup"><span data-stu-id="086c7-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="086c7-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="086c7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="086c7-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="086c7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="086c7-109">Simuliert, dass eine Taste gedrückt und anschließend freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="086c7-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="086c7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="086c7-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="086c7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="086c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="086c7-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="086c7-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="086c7-113">Der Schlüsselcode für den Schlüssel, der gedrückt und freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="086c7-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="086c7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="086c7-114">Return value</span></span>

<span data-ttu-id="086c7-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="086c7-115">This method can return one of these values.</span></span>



| <span data-ttu-id="086c7-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="086c7-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="086c7-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="086c7-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="086c7-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="086c7-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="086c7-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="086c7-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="086c7-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="086c7-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="086c7-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="086c7-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="086c7-122"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="086c7-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="086c7-123">Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.</span><span class="sxs-lookup"><span data-stu-id="086c7-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="086c7-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="086c7-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="086c7-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="086c7-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="086c7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="086c7-126">Requirements</span></span>



| <span data-ttu-id="086c7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="086c7-127">Requirement</span></span> | <span data-ttu-id="086c7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="086c7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="086c7-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="086c7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="086c7-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="086c7-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="086c7-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="086c7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="086c7-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="086c7-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="086c7-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="086c7-133">End of client support</span></span><br/>    | <span data-ttu-id="086c7-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="086c7-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="086c7-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="086c7-135">Product</span></span><br/>                  | <span data-ttu-id="086c7-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="086c7-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="086c7-137">Header</span><span class="sxs-lookup"><span data-stu-id="086c7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="086c7-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="086c7-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="086c7-139">IID</span><span class="sxs-lookup"><span data-stu-id="086c7-139">IID</span></span><br/>                      | <span data-ttu-id="086c7-140">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="086c7-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="086c7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="086c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086c7-142">**Ivmkeyboard**</span><span class="sxs-lookup"><span data-stu-id="086c7-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

