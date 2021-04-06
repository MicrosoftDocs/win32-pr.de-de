---
title: Ivmkeyboard-Methode ibuttssed (vpccominterfaces. h)
description: Bestimmt, ob der angegebene Schlüssel nicht angezeigt wird.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- Ispree-Methode Virtual PC
- Ispree-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, Iout-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742600"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="9efbb-106">Ivmkeyboard:: igestressed-Methode</span><span class="sxs-lookup"><span data-stu-id="9efbb-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="9efbb-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9efbb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9efbb-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9efbb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9efbb-109">Bestimmt, ob der angegebene Schlüssel nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9efbb-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="9efbb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9efbb-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="9efbb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9efbb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9efbb-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9efbb-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9efbb-113">Der Schlüsselcode für den Schlüssel, dessen Zustand abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9efbb-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="9efbb-114">*gedrückt* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9efbb-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9efbb-115">**True** , wenn der Schlüssel aktuell gedrückt ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9efbb-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9efbb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9efbb-116">Return value</span></span>

<span data-ttu-id="9efbb-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9efbb-117">This method can return one of these values.</span></span>



| <span data-ttu-id="9efbb-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9efbb-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="9efbb-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9efbb-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9efbb-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9efbb-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9efbb-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9efbb-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9efbb-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9efbb-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9efbb-123">Ein Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="9efbb-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="9efbb-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9efbb-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="9efbb-125">Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.</span><span class="sxs-lookup"><span data-stu-id="9efbb-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="9efbb-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9efbb-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9efbb-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9efbb-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="9efbb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9efbb-128">Requirements</span></span>



| <span data-ttu-id="9efbb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9efbb-129">Requirement</span></span> | <span data-ttu-id="9efbb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9efbb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9efbb-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9efbb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9efbb-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9efbb-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9efbb-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9efbb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9efbb-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9efbb-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9efbb-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9efbb-135">End of client support</span></span><br/>    | <span data-ttu-id="9efbb-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9efbb-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9efbb-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="9efbb-137">Product</span></span><br/>                  | <span data-ttu-id="9efbb-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9efbb-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9efbb-139">Header</span><span class="sxs-lookup"><span data-stu-id="9efbb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9efbb-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9efbb-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9efbb-141">IID</span><span class="sxs-lookup"><span data-stu-id="9efbb-141">IID</span></span><br/>                      | <span data-ttu-id="9efbb-142">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="9efbb-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="9efbb-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9efbb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efbb-144">**Ivmkeyboard**</span><span class="sxs-lookup"><span data-stu-id="9efbb-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

