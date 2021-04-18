---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der den Vergleich (in der Karte) der Überprüfungs Daten initiiert, die vom Schnittstellen Gerät mit den Verweis Daten, die auf der Karte gespeichert sind (z. b. Password), gesendet werden.
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816:: Verify-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348083"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="870a5-103">ISCardISO7816:: Verify-Methode</span><span class="sxs-lookup"><span data-stu-id="870a5-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="870a5-104">\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="870a5-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="870a5-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="870a5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="870a5-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="870a5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="870a5-107">Die **Verify** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der den Vergleich (auf der Karte) der Überprüfungs Daten initiiert, die vom Schnittstellen Gerät mit den Verweis Daten, die auf der Karte gespeichert sind (z. b. Password), gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="870a5-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="870a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="870a5-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="870a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="870a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="870a5-110">*ByRef STRG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="870a5-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="870a5-111">Ein Quantifizierer der Verweis Daten.</span><span class="sxs-lookup"><span data-stu-id="870a5-111">A quantifier of the reference data.</span></span> <span data-ttu-id="870a5-112">Das Codieren des Verweis Steuer Elements P2 folgt.</span><span class="sxs-lookup"><span data-stu-id="870a5-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="870a5-113">Wenn der Text leer ist, kann der Befehl entweder zum Abrufen der Zahl "X" der weiteren zulässigen Wiederholungen (SW1-SW2 = 63CX) oder zum Überprüfen, ob die Überprüfung nicht erforderlich ist (SW1-SW2 = 9000), verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="870a5-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="870a5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="870a5-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="870a5-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="870a5-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="870a5-116"><dt>**Keine Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="870a5-117">Bitposition: 00000000</span><span class="sxs-lookup"><span data-stu-id="870a5-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="870a5-118">P2 = 00 gibt an, dass kein bestimmter Qualifizierer auf den Karten verwendet wird, an denen der Verify-Befehl eindeutig auf die geheimen Daten verweist.</span><span class="sxs-lookup"><span data-stu-id="870a5-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="870a5-119"><dt>**Globaler Verweis**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="870a5-120">Bitposition: 0-------</span><span class="sxs-lookup"><span data-stu-id="870a5-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="870a5-121">Ein Beispiel für einen globalen Verweis wäre ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="870a5-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="870a5-122"><dt>**Spezifischer Verweis**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="870a5-123">Bitposition: 1-------</span><span class="sxs-lookup"><span data-stu-id="870a5-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="870a5-124">Ein Beispiel für einen bestimmten Verweis ist ein DF-spezifisches Kennwort.</span><span class="sxs-lookup"><span data-stu-id="870a5-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="870a5-125"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="870a5-126">Bitposition:-XX-----</span><span class="sxs-lookup"><span data-stu-id="870a5-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="870a5-127"><dt>**Verweis Daten \#**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="870a5-128">Bitposition:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="870a5-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="870a5-129">Die Verweis Daten Nummer kann z. b. eine Kenn Wort Nummer oder eine kurze EF-ID sein.</span><span class="sxs-lookup"><span data-stu-id="870a5-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="870a5-130">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="870a5-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="870a5-131">Ein Zeiger auf die Überprüfungs Daten.</span><span class="sxs-lookup"><span data-stu-id="870a5-131">A pointer to the verification data.</span></span> <span data-ttu-id="870a5-132">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="870a5-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="870a5-133">Der Standardwert ist **NULL**.</span><span class="sxs-lookup"><span data-stu-id="870a5-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="870a5-134">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="870a5-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="870a5-135">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="870a5-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="870a5-136">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="870a5-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="870a5-137">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mithilfe des *ppcmd* -Zeigers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="870a5-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="870a5-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="870a5-138">Return value</span></span>

<span data-ttu-id="870a5-139">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="870a5-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="870a5-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="870a5-140">Return code</span></span>                                                                                   | <span data-ttu-id="870a5-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="870a5-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="870a5-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="870a5-143">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="870a5-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="870a5-144"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="870a5-145">Es wurde ein ungültiger Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="870a5-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="870a5-146"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="870a5-147">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="870a5-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="870a5-148"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="870a5-149">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="870a5-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="870a5-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="870a5-150">Remarks</span></span>

<span data-ttu-id="870a5-151">Der Sicherheitsstatus kann aufgrund eines Vergleichs geändert werden.</span><span class="sxs-lookup"><span data-stu-id="870a5-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="870a5-152">Nicht erfolgreiche Vergleiche können auf der Karte aufgezeichnet werden (z. b. um die Anzahl der weiteren Versuche der Verwendung der Verweis Daten einzuschränken).</span><span class="sxs-lookup"><span data-stu-id="870a5-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="870a5-153">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="870a5-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="870a5-154">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="870a5-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="870a5-155">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="870a5-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="870a5-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="870a5-156">Requirements</span></span>



| <span data-ttu-id="870a5-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="870a5-157">Requirement</span></span> | <span data-ttu-id="870a5-158">Wert</span><span class="sxs-lookup"><span data-stu-id="870a5-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="870a5-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="870a5-159">Minimum supported client</span></span><br/> | <span data-ttu-id="870a5-160">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="870a5-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="870a5-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="870a5-161">Minimum supported server</span></span><br/> | <span data-ttu-id="870a5-162">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="870a5-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="870a5-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="870a5-163">End of client support</span></span><br/>    | <span data-ttu-id="870a5-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="870a5-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="870a5-165">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="870a5-165">End of server support</span></span><br/>    | <span data-ttu-id="870a5-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="870a5-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="870a5-167">Header</span><span class="sxs-lookup"><span data-stu-id="870a5-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="870a5-168"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="870a5-169">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="870a5-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="870a5-170"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="870a5-171">DLL</span><span class="sxs-lookup"><span data-stu-id="870a5-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="870a5-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="870a5-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="870a5-173">IID</span><span class="sxs-lookup"><span data-stu-id="870a5-173">IID</span></span><br/>                      | <span data-ttu-id="870a5-174">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="870a5-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="870a5-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="870a5-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870a5-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="870a5-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
