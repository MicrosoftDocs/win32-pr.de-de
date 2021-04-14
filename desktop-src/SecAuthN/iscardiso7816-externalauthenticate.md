---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der den Sicherheitsstatus bedingt aktualisiert und die Identität des Computers überprüft, wenn Sie von der Smartcard nicht als vertrauenswürdig eingestuft wird.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816:: externalauthenticate-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393550"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="784cc-103">ISCardISO7816:: externalauthenticate-Methode</span><span class="sxs-lookup"><span data-stu-id="784cc-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="784cc-104">\[Die **externalauthenticate** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="784cc-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="784cc-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="784cc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="784cc-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="784cc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="784cc-107">Die **externalauthenticate** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der den Sicherheitsstatus bedingt aktualisiert und die Identität des Computers überprüft, wenn Sie von der [*Smartcard*](../secgloss/s-gly.md) nicht als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="784cc-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="784cc-108">Der Befehl verwendet das Ergebnis (ja oder Nein) der Berechnung durch die Karte (basierend auf einer Herausforderung, die zuvor von der Karte ausgegeben wurde, z. b. mit dem Befehl "in \_ get \_ Challenge"), einem Schlüssel (möglicherweise geheimer Schlüssel), der auf der Karte gespeichert ist, und vom Schnittstellen Gerät übertragene Authentifizierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="784cc-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="784cc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="784cc-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="784cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="784cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="784cc-111">*byalgorithmref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="784cc-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="784cc-112">Der Verweis auf den Algorithmus in der Karte.</span><span class="sxs-lookup"><span data-stu-id="784cc-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="784cc-113">Wenn dieser Wert 0 (null) ist, bedeutet dies, dass keine Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="784cc-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="784cc-114">Der Verweis auf den Algorithmus ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="784cc-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="784cc-115">*bysecretref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="784cc-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="784cc-116">Der Verweis auf das Geheimnis.</span><span class="sxs-lookup"><span data-stu-id="784cc-116">The reference of the secret.</span></span>



| <span data-ttu-id="784cc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="784cc-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="784cc-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="784cc-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="784cc-119"><dt>**Keine Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="784cc-120">Bitposition: 00000000</span><span class="sxs-lookup"><span data-stu-id="784cc-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="784cc-121">Es werden keine Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="784cc-121">No information is given.</span></span> <span data-ttu-id="784cc-122">Der Verweis auf das Geheimnis ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="784cc-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="784cc-123"><dt>**Globaler Verweis**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="784cc-124">Bitposition: 0-------</span><span class="sxs-lookup"><span data-stu-id="784cc-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="784cc-125">Globale Verweis Daten (ein für die MF spezifischer Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="784cc-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="784cc-126"><dt>**Spezifischer Verweis**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="784cc-127">Bitposition: 1-------</span><span class="sxs-lookup"><span data-stu-id="784cc-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="784cc-128">Bestimmte Verweis Daten (ein DF-spezifischer Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="784cc-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="784cc-129"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="784cc-130">Bitposition:-XX-----</span><span class="sxs-lookup"><span data-stu-id="784cc-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="784cc-131">00 (andere Werte sind RFU).</span><span class="sxs-lookup"><span data-stu-id="784cc-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="784cc-132"><dt>**Geheimen**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="784cc-133">Bitposition:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="784cc-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="784cc-134">Die Nummer des Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="784cc-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="784cc-135">*pchallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="784cc-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="784cc-136">Ein Zeiger auf die Authentifizierungs bezogenen Daten.</span><span class="sxs-lookup"><span data-stu-id="784cc-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="784cc-137">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="784cc-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="784cc-138">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="784cc-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="784cc-139">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="784cc-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="784cc-140">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="784cc-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="784cc-141">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mithilfe des *ppcmd* -Zeigers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="784cc-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="784cc-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="784cc-142">Return value</span></span>

<span data-ttu-id="784cc-143">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="784cc-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="784cc-144">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="784cc-144">Return code</span></span>                                                                                   | <span data-ttu-id="784cc-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="784cc-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="784cc-146"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="784cc-147">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="784cc-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="784cc-148"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="784cc-149">Ein ungültiger Parameter wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="784cc-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="784cc-150"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="784cc-151">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="784cc-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="784cc-152"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="784cc-153">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="784cc-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="784cc-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="784cc-154">Remarks</span></span>

<span data-ttu-id="784cc-155">Damit der gekapselte Befehl erfolgreich ausgeführt werden kann, muss die letzte von der Karte erhaltene Abfrage gültig sein.</span><span class="sxs-lookup"><span data-stu-id="784cc-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="784cc-156">Nicht erfolgreiche Vergleiche können auf der Karte aufgezeichnet werden (z. b. um die Anzahl der weiteren Versuche der Verwendung der Verweis Daten einzuschränken).</span><span class="sxs-lookup"><span data-stu-id="784cc-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="784cc-157">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="784cc-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="784cc-158">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="784cc-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="784cc-159">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="784cc-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="784cc-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="784cc-160">Requirements</span></span>



| <span data-ttu-id="784cc-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="784cc-161">Requirement</span></span> | <span data-ttu-id="784cc-162">Wert</span><span class="sxs-lookup"><span data-stu-id="784cc-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="784cc-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="784cc-163">Minimum supported client</span></span><br/> | <span data-ttu-id="784cc-164">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="784cc-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="784cc-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="784cc-165">Minimum supported server</span></span><br/> | <span data-ttu-id="784cc-166">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="784cc-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="784cc-167">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="784cc-167">End of client support</span></span><br/>    | <span data-ttu-id="784cc-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="784cc-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="784cc-169">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="784cc-169">End of server support</span></span><br/>    | <span data-ttu-id="784cc-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="784cc-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="784cc-171">Header</span><span class="sxs-lookup"><span data-stu-id="784cc-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="784cc-172"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="784cc-173">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="784cc-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="784cc-174"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="784cc-175">DLL</span><span class="sxs-lookup"><span data-stu-id="784cc-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="784cc-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="784cc-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="784cc-177">IID</span><span class="sxs-lookup"><span data-stu-id="784cc-177">IID</span></span><br/>                      | <span data-ttu-id="784cc-178">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="784cc-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="784cc-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="784cc-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784cc-180">**Internalauthenticate**</span><span class="sxs-lookup"><span data-stu-id="784cc-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="784cc-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="784cc-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
