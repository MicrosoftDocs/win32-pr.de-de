---
title: Ivmkeyboard typekeysequence-Methode (vpccominterfaces. h)
description: Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die eingegeben werden.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Typekeysequence-Methode Virtual PC
- Typekeysequence-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, typekeysequence-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957122"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="bdefc-106">Ivmkeyboard:: typekeysequence-Methode</span><span class="sxs-lookup"><span data-stu-id="bdefc-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="bdefc-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdefc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bdefc-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bdefc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bdefc-109">Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bdefc-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdefc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdefc-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="bdefc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdefc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdefc-112">*keysequence* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdefc-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdefc-113">Die durch Trennzeichen getrennte Sequenz von Schlüsselcodes, die eingegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bdefc-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdefc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdefc-114">Return value</span></span>

<span data-ttu-id="bdefc-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bdefc-115">This method can return one of these values.</span></span>



| <span data-ttu-id="bdefc-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bdefc-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="bdefc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdefc-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bdefc-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bdefc-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bdefc-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdefc-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bdefc-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bdefc-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bdefc-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bdefc-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="bdefc-122"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bdefc-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="bdefc-123">Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.</span><span class="sxs-lookup"><span data-stu-id="bdefc-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="bdefc-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bdefc-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bdefc-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bdefc-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="bdefc-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdefc-126">Remarks</span></span>

<span data-ttu-id="bdefc-127">Eine Schlüssel Sequenz Zeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüssel Bezeichnerzeichen, die verwendet werden, um die Tastenkombination und die releasesequenz einer Standardtastatur des US-amerikanischen 101-Schlüssels zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="bdefc-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="bdefc-128">Wenn ein Schlüssel Bezeichner in der Zeichenfolge ohne einen vorangehenden Modifizierer angezeigt wird, wird ein mit Schlüsseln gedrückter Code an die Sitzung der virtuellen Maschine gesendet, gefolgt von dem zugehörigen Schlüsselcode.</span><span class="sxs-lookup"><span data-stu-id="bdefc-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="bdefc-129">Schlüsselmodifizierer können verwendet werden, um dieses Verhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bdefc-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="bdefc-130">Der Down-Modifizierer sendet z. b. den Schlüssel gesteuerten Code für den folgenden Schlüssel Bezeichner, ohne den Schlüssel freigegebenen Code zu senden.</span><span class="sxs-lookup"><span data-stu-id="bdefc-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="bdefc-131">Dies ist nützlich zum Simulieren von STRG-, alt-und Umschalttaste, wenn Sie gedrückt werden, während andere Schlüssel gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdefc-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="bdefc-132">Um den Schlüssel freizugeben, muss er erneut in die Schlüssel Zeichenfolge eingefügt werden, zusammen mit einem vorangehenden Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="bdefc-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdefc-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdefc-133">Requirements</span></span>



| <span data-ttu-id="bdefc-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdefc-134">Requirement</span></span> | <span data-ttu-id="bdefc-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bdefc-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdefc-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdefc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bdefc-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdefc-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bdefc-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdefc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bdefc-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bdefc-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bdefc-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bdefc-140">End of client support</span></span><br/>    | <span data-ttu-id="bdefc-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bdefc-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bdefc-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="bdefc-142">Product</span></span><br/>                  | <span data-ttu-id="bdefc-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bdefc-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bdefc-144">Header</span><span class="sxs-lookup"><span data-stu-id="bdefc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdefc-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdefc-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bdefc-146">IID</span><span class="sxs-lookup"><span data-stu-id="bdefc-146">IID</span></span><br/>                      | <span data-ttu-id="bdefc-147">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="bdefc-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bdefc-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdefc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdefc-149">**Ivmkeyboard**</span><span class="sxs-lookup"><span data-stu-id="bdefc-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="bdefc-150">Schlüsselsequenzen</span><span class="sxs-lookup"><span data-stu-id="bdefc-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

