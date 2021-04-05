---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der die Berechnung der Authentifizierungsdaten durch die Karte mit den vom Schnittstellen Gerät gesendeten Abfrage Daten und einem relevanten geheimen Schlüssel (z. b. einem Schlüssel) initiiert, der in der Karte gespeichert ist.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816:: internalauthenticate-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042067"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="40d4c-103">ISCardISO7816:: internalauthenticate-Methode</span><span class="sxs-lookup"><span data-stu-id="40d4c-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="40d4c-104">\[Die **internalauthenticate** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="40d4c-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="40d4c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40d4c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="40d4c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="40d4c-107">Die **internalauthenticate** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der die Berechnung der Authentifizierungsdaten durch die Karte initiiert, indem die vom Schnittstellen Gerät gesendeten Anforderungs Daten und ein relevanter geheimer Schlüssel (z. b. ein Schlüssel) auf der Karte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="40d4c-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="40d4c-108">Wenn das relevante Geheimnis an das MF angehängt ist, kann der Befehl verwendet werden, um die Karte als Ganzes zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="40d4c-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="40d4c-109">Wenn das relevante Geheimnis an eine andere DF angefügt ist, kann der Befehl zum Authentifizieren der DF verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40d4c-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d4c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="40d4c-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="40d4c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="40d4c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d4c-112">*byalgorithmref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d4c-113">Verweis auf den Algorithmus in der Karte.</span><span class="sxs-lookup"><span data-stu-id="40d4c-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="40d4c-114">Wenn dieser Wert 0 (null) ist, bedeutet dies, dass keine Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="40d4c-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="40d4c-115">Der Verweis auf den Algorithmus ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="40d4c-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="40d4c-116">*bysecretref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d4c-117">Verweis auf den geheimen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="40d4c-117">Reference of the secret.</span></span>



| <span data-ttu-id="40d4c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="40d4c-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="40d4c-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="40d4c-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="40d4c-120"><dt>**Keine Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="40d4c-121">Bitposition: 00000000</span><span class="sxs-lookup"><span data-stu-id="40d4c-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="40d4c-122">Es werden keine Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="40d4c-122">No information is given.</span></span> <span data-ttu-id="40d4c-123">Der Verweis auf das Geheimnis ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="40d4c-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="40d4c-124"><dt>**Globaler Verweis**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="40d4c-125">Bitposition: 0-------</span><span class="sxs-lookup"><span data-stu-id="40d4c-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="40d4c-126">Globale Verweis Daten (ein für die MF spezifischer Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="40d4c-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="40d4c-127"><dt>**Spezifischer Verweis**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="40d4c-128">Bitposition: 1-------</span><span class="sxs-lookup"><span data-stu-id="40d4c-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="40d4c-129">Bestimmte Verweis Daten (ein DF-spezifischer Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="40d4c-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="40d4c-130"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="40d4c-131">Bitposition:-XX-----</span><span class="sxs-lookup"><span data-stu-id="40d4c-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="40d4c-132">00 (andere Werte sind RFU).</span><span class="sxs-lookup"><span data-stu-id="40d4c-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="40d4c-133"><dt>**Geheimen**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="40d4c-134">Bitposition:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="40d4c-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="40d4c-135">Die Nummer des Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="40d4c-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="40d4c-136">*pchallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d4c-137">Zeiger auf die Authentifizierungs bezogenen Daten (z. b. "Challenge").</span><span class="sxs-lookup"><span data-stu-id="40d4c-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="40d4c-138">*lreplybytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d4c-139">Maximale Anzahl von Bytes, die als Antwort erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="40d4c-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="40d4c-140">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40d4c-141">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="40d4c-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="40d4c-142">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="40d4c-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="40d4c-143">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40d4c-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d4c-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40d4c-144">Return value</span></span>

<span data-ttu-id="40d4c-145">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="40d4c-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="40d4c-146">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="40d4c-146">Return code</span></span>                                                                                   | <span data-ttu-id="40d4c-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40d4c-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="40d4c-148"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="40d4c-149">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="40d4c-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="40d4c-150"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="40d4c-151">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="40d4c-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="40d4c-152"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="40d4c-153">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="40d4c-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="40d4c-154"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="40d4c-155">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="40d4c-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="40d4c-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40d4c-156">Remarks</span></span>

<span data-ttu-id="40d4c-157">Die erfolgreiche Ausführung des Befehls kann dem erfolgreichen Abschluss vorheriger Befehle (z. b. überprüfen oder auswählen der Datei) oder der Auswahl (z. b. des relevanten Geheimnisses) unterliegen.</span><span class="sxs-lookup"><span data-stu-id="40d4c-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="40d4c-158">Wenn beim Ausgeben des Befehls eine Taste und ein Algorithmus ausgewählt sind, verwendet der Befehl möglicherweise implizit den Schlüssel und den Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="40d4c-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="40d4c-159">Die Häufigkeit, mit der der Befehl ausgegeben wird, kann in der Karte aufgezeichnet werden, um die Anzahl der weiteren Versuche der Verwendung des relevanten Geheimnisses oder des Algorithmus einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="40d4c-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="40d4c-160">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="40d4c-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="40d4c-161">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="40d4c-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="40d4c-162">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="40d4c-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40d4c-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40d4c-163">Requirements</span></span>



| <span data-ttu-id="40d4c-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40d4c-164">Requirement</span></span> | <span data-ttu-id="40d4c-165">Wert</span><span class="sxs-lookup"><span data-stu-id="40d4c-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d4c-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40d4c-166">Minimum supported client</span></span><br/> | <span data-ttu-id="40d4c-167">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="40d4c-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40d4c-168">Minimum supported server</span></span><br/> | <span data-ttu-id="40d4c-169">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40d4c-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40d4c-170">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="40d4c-170">End of client support</span></span><br/>    | <span data-ttu-id="40d4c-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="40d4c-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="40d4c-172">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="40d4c-172">End of server support</span></span><br/>    | <span data-ttu-id="40d4c-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40d4c-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="40d4c-174">Header</span><span class="sxs-lookup"><span data-stu-id="40d4c-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d4c-175"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40d4c-176">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="40d4c-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="40d4c-177"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40d4c-178">DLL</span><span class="sxs-lookup"><span data-stu-id="40d4c-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d4c-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d4c-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="40d4c-180">IID</span><span class="sxs-lookup"><span data-stu-id="40d4c-180">IID</span></span><br/>                      | <span data-ttu-id="40d4c-181">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="40d4c-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="40d4c-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40d4c-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d4c-183">**Externalauthenticate**</span><span class="sxs-lookup"><span data-stu-id="40d4c-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="40d4c-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="40d4c-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
