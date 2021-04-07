---
description: Die GetData-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der je nach ausgewähltem Dateityp entweder ein einzelnes Primitives Datenobjekt oder einen Satz von Datenobjekten (in einem konstruierten Datenobjekt enthalten) abruft.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816:: GetData-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758095"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="94ca7-103">ISCardISO7816:: GetData-Methode</span><span class="sxs-lookup"><span data-stu-id="94ca7-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="94ca7-104">\[Die **GetData** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="94ca7-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="94ca7-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94ca7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94ca7-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="94ca7-107">Die **GetData** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der je nach ausgewähltem Dateityp entweder ein einzelnes Primitives Datenobjekt oder einen Satz von Datenobjekten (in einem konstruierten Datenobjekt enthalten) abruft.</span><span class="sxs-lookup"><span data-stu-id="94ca7-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ca7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="94ca7-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="94ca7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="94ca7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ca7-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ca7-111">Parameter.</span><span class="sxs-lookup"><span data-stu-id="94ca7-111">Parameters.</span></span>



| <span data-ttu-id="94ca7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="94ca7-112">Value</span></span>                                                                                  | <span data-ttu-id="94ca7-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94ca7-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="94ca7-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="94ca7-115">RFU</span><span class="sxs-lookup"><span data-stu-id="94ca7-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="94ca7-116"><dt>0040 Uhr</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-117">BER-TLV-Tag (1 Byte) in P2</span><span class="sxs-lookup"><span data-stu-id="94ca7-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="94ca7-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-119">Anwendungsdaten (proprietäre Codierung)</span><span class="sxs-lookup"><span data-stu-id="94ca7-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="94ca7-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-121">Simple-TLV-Tag in P2</span><span class="sxs-lookup"><span data-stu-id="94ca7-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="94ca7-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-123">RFU</span><span class="sxs-lookup"><span data-stu-id="94ca7-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="94ca7-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-125">BER-TLV-Tag (2 Bytes) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="94ca7-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="94ca7-126">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ca7-127">Parameter.</span><span class="sxs-lookup"><span data-stu-id="94ca7-127">Parameters.</span></span>



| <span data-ttu-id="94ca7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="94ca7-128">Value</span></span>                                                                                  | <span data-ttu-id="94ca7-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94ca7-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="94ca7-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="94ca7-131">RFU</span><span class="sxs-lookup"><span data-stu-id="94ca7-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="94ca7-132"><dt>0040 Uhr</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-133">BER-TLV-Tag (1 Byte) in P2</span><span class="sxs-lookup"><span data-stu-id="94ca7-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="94ca7-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-135">Anwendungsdaten (proprietäre Codierung)</span><span class="sxs-lookup"><span data-stu-id="94ca7-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="94ca7-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-137">Simple-TLV-Tag in P2</span><span class="sxs-lookup"><span data-stu-id="94ca7-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="94ca7-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-139">RFU</span><span class="sxs-lookup"><span data-stu-id="94ca7-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="94ca7-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="94ca7-141">BER-TLV-Tag (2 Bytes) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="94ca7-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="94ca7-142">*lbytestoget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ca7-143">Anzahl von Bytes, die in der Antwort erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="94ca7-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="94ca7-144">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="94ca7-145">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="94ca7-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="94ca7-146">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="94ca7-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="94ca7-147">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94ca7-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ca7-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94ca7-148">Return value</span></span>

<span data-ttu-id="94ca7-149">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="94ca7-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="94ca7-150">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="94ca7-150">Return code</span></span>                                                                                   | <span data-ttu-id="94ca7-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94ca7-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="94ca7-152"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="94ca7-153">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="94ca7-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="94ca7-154"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="94ca7-155">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="94ca7-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="94ca7-156"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="94ca7-157">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="94ca7-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="94ca7-158"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="94ca7-159">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="94ca7-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="94ca7-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94ca7-160">Remarks</span></span>

<span data-ttu-id="94ca7-161">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu lesenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="94ca7-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="94ca7-162">Sicherheitsbedingungen sind von der Richtlinie der Karte abhängig und können durch [**externalauthenticate**](iscardiso7816-externalauthenticate.md), [**internalauthenticate**](iscardiso7816-internalauthenticate.md), [**iscardauth**](iscardauth.md)usw. manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="94ca7-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="94ca7-163">Um eine Datei auszuwählen, wählen Sie [**selectfile**](iscardiso7816-selectfile.md)aus.</span><span class="sxs-lookup"><span data-stu-id="94ca7-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="94ca7-164">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="94ca7-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="94ca7-165">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="94ca7-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="94ca7-166">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="94ca7-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94ca7-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94ca7-167">Requirements</span></span>



| <span data-ttu-id="94ca7-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94ca7-168">Requirement</span></span> | <span data-ttu-id="94ca7-169">Wert</span><span class="sxs-lookup"><span data-stu-id="94ca7-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94ca7-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94ca7-170">Minimum supported client</span></span><br/> | <span data-ttu-id="94ca7-171">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="94ca7-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94ca7-172">Minimum supported server</span></span><br/> | <span data-ttu-id="94ca7-173">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94ca7-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94ca7-174">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="94ca7-174">End of client support</span></span><br/>    | <span data-ttu-id="94ca7-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="94ca7-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="94ca7-176">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="94ca7-176">End of server support</span></span><br/>    | <span data-ttu-id="94ca7-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="94ca7-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="94ca7-178">Header</span><span class="sxs-lookup"><span data-stu-id="94ca7-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ca7-179"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="94ca7-180">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="94ca7-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="94ca7-181"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="94ca7-182">DLL</span><span class="sxs-lookup"><span data-stu-id="94ca7-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94ca7-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94ca7-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="94ca7-184">IID</span><span class="sxs-lookup"><span data-stu-id="94ca7-184">IID</span></span><br/>                      | <span data-ttu-id="94ca7-185">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="94ca7-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="94ca7-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94ca7-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ca7-187">**Externalauthenticate**</span><span class="sxs-lookup"><span data-stu-id="94ca7-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="94ca7-188">**Internalauthenticate**</span><span class="sxs-lookup"><span data-stu-id="94ca7-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="94ca7-189">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="94ca7-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="94ca7-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="94ca7-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="94ca7-191">**Putdata**</span><span class="sxs-lookup"><span data-stu-id="94ca7-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="94ca7-192">**Selectfile**</span><span class="sxs-lookup"><span data-stu-id="94ca7-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
