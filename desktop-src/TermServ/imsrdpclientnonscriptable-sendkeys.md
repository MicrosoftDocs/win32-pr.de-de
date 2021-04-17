---
title: Imsrdpclientnonscriptable SendKeys-Methode
description: Sendet eine Reihe von Tastatureingaben an das-Steuerelement. Die Tastatureingaben befinden sich in einem Scan-codeformular, bei dem es sich um die Tastatur Daten aus den eigentlichen physischen Schlüsseln handelt.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys-Methode Remotedesktopdienste
- SendKeys-Methode Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, SendKeys-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477766"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="953fe-115">Imsrdpclientnonscriptable:: SendKeys-Methode</span><span class="sxs-lookup"><span data-stu-id="953fe-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="953fe-116">Sendet eine Reihe von Tastatureingaben an das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="953fe-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="953fe-117">Die Tastatureingaben befinden sich in einem Scan-codeformular, bei dem es sich um die Tastatur Daten aus den eigentlichen physischen Schlüsseln handelt.</span><span class="sxs-lookup"><span data-stu-id="953fe-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="953fe-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="953fe-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="953fe-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="953fe-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="953fe-120">*numKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="953fe-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953fe-121">Die Anzahl der zu sendenden Tastatureingaben.</span><span class="sxs-lookup"><span data-stu-id="953fe-121">The number of keystrokes to send.</span></span> <span data-ttu-id="953fe-122">Die maximale Anzahl von Schlüsseln, die in einem Vorgang gesendet werden können, beträgt 20.</span><span class="sxs-lookup"><span data-stu-id="953fe-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="953fe-123">Die Methode gibt **E \_ invalidArg** zurück, wenn dieser Parameter größer als 20 ist.</span><span class="sxs-lookup"><span data-stu-id="953fe-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="953fe-124">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="953fe-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="953fe-125">*pbarraykeyup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="953fe-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953fe-126">Ein Array, dessen Größe gleich *numKeys* ist.</span><span class="sxs-lookup"><span data-stu-id="953fe-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="953fe-127">Ein Element ist " **true** ", wenn der entsprechende Schlüssel auf dem neuesten Stand ist, und " **false** ", wenn der entsprechende Schlüssel nicht</span><span class="sxs-lookup"><span data-stu-id="953fe-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="953fe-128">*plkeydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="953fe-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953fe-129">Ein Array, dessen Größe gleich *numKeys* ist.</span><span class="sxs-lookup"><span data-stu-id="953fe-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="953fe-130">Das Array enthält Tastatureingabe-Daten und entspricht dem Wert des *LPARAM* -Parameters der [WM- \_ KeyDown](../inputdev/wm-keydown.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="953fe-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="953fe-131">Die Daten geben die Wiederholungs Anzahl, den Überprüfungs Code, das erweiterte schlüsselflag, den Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand an.</span><span class="sxs-lookup"><span data-stu-id="953fe-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="953fe-132">Eine Beschreibung der Bits in diesem Array finden [Sie unter WM- \_ KeyDown](../inputdev/wm-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="953fe-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="953fe-133">Das entsprechende Element in *pbarraykeyup* gibt an, ob der Schlüssel nach oben oder unten ist.</span><span class="sxs-lookup"><span data-stu-id="953fe-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="953fe-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="953fe-134">Return value</span></span>

<span data-ttu-id="953fe-135">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="953fe-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="953fe-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="953fe-136">Remarks</span></span>

<span data-ttu-id="953fe-137">Die **SendKeys** -Methode vermischt keine Tastatureingaben, die vom lokalen Benutzer mit Tastatureingaben durchgeführt werden, die von der Methode gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="953fe-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="953fe-138">Alle an die-Methode weiter gegebenen Tastatureingaben werden in einer einzelnen atomarischen Sequenz an die Remote Sitzung gesendet.</span><span class="sxs-lookup"><span data-stu-id="953fe-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="953fe-139">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="953fe-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="953fe-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="953fe-140">Requirements</span></span>



| <span data-ttu-id="953fe-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="953fe-141">Requirement</span></span> | <span data-ttu-id="953fe-142">Wert</span><span class="sxs-lookup"><span data-stu-id="953fe-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="953fe-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="953fe-143">Minimum supported client</span></span><br/> | <span data-ttu-id="953fe-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="953fe-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="953fe-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="953fe-145">Minimum supported server</span></span><br/> | <span data-ttu-id="953fe-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="953fe-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="953fe-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="953fe-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="953fe-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="953fe-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="953fe-149">DLL</span><span class="sxs-lookup"><span data-stu-id="953fe-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="953fe-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="953fe-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="953fe-151">IID</span><span class="sxs-lookup"><span data-stu-id="953fe-151">IID</span></span><br/>                      | <span data-ttu-id="953fe-152">IID \_ imsrdpclientnonscriptable ist als 2f079c4c-87b2-4afd-97ab-20cdb43038ae definiert.</span><span class="sxs-lookup"><span data-stu-id="953fe-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="953fe-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="953fe-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953fe-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="953fe-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="953fe-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="953fe-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="953fe-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="953fe-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="953fe-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="953fe-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="953fe-158">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="953fe-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="953fe-159">WM- \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="953fe-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

