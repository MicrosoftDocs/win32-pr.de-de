---
description: Die putdata-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), mit dem ein einzelnes Primitives Datenobjekt oder der Satz von Datenobjekten, die in einem konstruierten Datenobjekt enthalten sind, abhängig von der ausgewählten Datei gespeichert wird.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816::P utdata-Methode (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866996"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="097da-103">ISCardISO7816::P utdata-Methode</span><span class="sxs-lookup"><span data-stu-id="097da-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="097da-104">\[Die **putdata** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="097da-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="097da-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="097da-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="097da-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="097da-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="097da-107">Die **putdata** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), mit dem ein einzelnes Primitives Datenobjekt oder der Satz von Datenobjekten, die in einem konstruierten Datenobjekt enthalten sind, abhängig von der ausgewählten Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="097da-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="097da-108">Wie die Objekte gespeichert werden (das einmalige schreiben und/oder aktualisieren und/oder Anhängen), hängt von der Definition oder der Art der Datenobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="097da-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="097da-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="097da-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="097da-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="097da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097da-111">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="097da-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097da-112">Codieren von P1-P2.</span><span class="sxs-lookup"><span data-stu-id="097da-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="097da-113">Wert</span><span class="sxs-lookup"><span data-stu-id="097da-113">Value</span></span>                                                                                  | <span data-ttu-id="097da-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="097da-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="097da-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="097da-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="097da-116">RFU</span><span class="sxs-lookup"><span data-stu-id="097da-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="097da-117"><dt>0040 Uhr</dt></span><span class="sxs-lookup"><span data-stu-id="097da-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="097da-118">BER-TLV-Tag (1 Byte) in P2</span><span class="sxs-lookup"><span data-stu-id="097da-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="097da-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="097da-120">Anwendungsdaten (proprietäre Codierung)</span><span class="sxs-lookup"><span data-stu-id="097da-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="097da-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="097da-122">Simple-TLV-Tag in P2</span><span class="sxs-lookup"><span data-stu-id="097da-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="097da-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="097da-124">RFU</span><span class="sxs-lookup"><span data-stu-id="097da-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="097da-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="097da-126">BER-TLV-Tag (2 Bytes) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="097da-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="097da-127">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="097da-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097da-128">Codieren von P1-P2.</span><span class="sxs-lookup"><span data-stu-id="097da-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="097da-129">Wert</span><span class="sxs-lookup"><span data-stu-id="097da-129">Value</span></span>                                                                                  | <span data-ttu-id="097da-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="097da-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="097da-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="097da-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="097da-132">RFU</span><span class="sxs-lookup"><span data-stu-id="097da-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="097da-133"><dt>0040 Uhr</dt></span><span class="sxs-lookup"><span data-stu-id="097da-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="097da-134">BER-TLV-Tag (1 Byte) in P2</span><span class="sxs-lookup"><span data-stu-id="097da-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="097da-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="097da-136">Anwendungsdaten (proprietäre Codierung)</span><span class="sxs-lookup"><span data-stu-id="097da-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="097da-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="097da-138">Simple-TLV-Tag in P2</span><span class="sxs-lookup"><span data-stu-id="097da-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="097da-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="097da-140">RFU</span><span class="sxs-lookup"><span data-stu-id="097da-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="097da-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="097da-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="097da-142">BER-TLV-Tag (2 Bytes) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="097da-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="097da-143">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="097da-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097da-144">Zeiger auf einen Byte Puffer, der die zu schreibenden Parameter und Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="097da-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="097da-145">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="097da-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="097da-146">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="097da-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="097da-147">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="097da-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="097da-148">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="097da-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097da-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="097da-149">Return value</span></span>

<span data-ttu-id="097da-150">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="097da-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="097da-151">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="097da-151">Return code</span></span>                                                                                   | <span data-ttu-id="097da-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="097da-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="097da-153"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="097da-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="097da-154">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="097da-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="097da-155"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="097da-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="097da-156">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="097da-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="097da-157"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="097da-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="097da-158">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="097da-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="097da-159"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="097da-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="097da-160">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="097da-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="097da-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="097da-161">Remarks</span></span>

<span data-ttu-id="097da-162">Der Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus den Sicherheitsbedingungen entspricht, die von der Anwendung innerhalb des [*Kontexts*](../secgloss/c-gly.md) für die Funktion definiert werden.</span><span class="sxs-lookup"><span data-stu-id="097da-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="097da-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Speichern von Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="097da-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="097da-164">Liegt der Wert von P1-P2 im Bereich von 0100 bis 01FF, muss der Wert von P1-P2 ein Bezeichnertyp sein, der für interne Karten Tests und für proprietäre Dienste reserviert ist, die innerhalb eines bestimmten Anwendungs Kontexts aussagekräftig sind.</span><span class="sxs-lookup"><span data-stu-id="097da-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="097da-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Speichern von Datenobjekten</span><span class="sxs-lookup"><span data-stu-id="097da-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="097da-166">Wenn der Wert P1-P2 im Bereich von 0040 bis 00FF liegt, muss P2 ein ber-TLV-Tag in einem einzelnen Byte sein.</span><span class="sxs-lookup"><span data-stu-id="097da-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="097da-167">Der Wert von 00FF ist dafür reserviert, anzugeben, dass das Datenfeld ber-TLV-Datenobjekte enthält.</span><span class="sxs-lookup"><span data-stu-id="097da-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="097da-168">Liegt der Wert von P1-P2 im Bereich von 0200 bis 02FF, muss P2 ein Simple-TLV-Tag sein.</span><span class="sxs-lookup"><span data-stu-id="097da-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="097da-169">Der Wert 0200 ist RFU.</span><span class="sxs-lookup"><span data-stu-id="097da-169">The value 0200 is RFU.</span></span> <span data-ttu-id="097da-170">Der Wert 02FF ist dafür reserviert, anzugeben, dass das Datenfeld einfache TLV-Datenobjekte enthält.</span><span class="sxs-lookup"><span data-stu-id="097da-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="097da-171">Liegt der Wert von P1-P2 im Bereich von 4000 bis FFFF, muss der Wert von P1-P2 ein ber-TLV-Tag mit zwei Bytes sein.</span><span class="sxs-lookup"><span data-stu-id="097da-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="097da-172">Die Werte 4000 bis FFFF sind RFU.</span><span class="sxs-lookup"><span data-stu-id="097da-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="097da-173">Wenn ein Primitives Datenobjekt bereitgestellt wird, muss das Datenfeld der Befehls Meldung den Wert des entsprechenden primitiven Datenobjekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="097da-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="097da-174">Wenn ein konstruiertes Datenobjekt bereitgestellt wird, muss das Datenfeld der Befehls Meldung den Wert des konstruierten Datenobjekts enthalten (d. h. Datenobjekte einschließlich Tag, Länge und Wert).</span><span class="sxs-lookup"><span data-stu-id="097da-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="097da-175">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="097da-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="097da-176">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="097da-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="097da-177">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="097da-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="097da-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="097da-178">Requirements</span></span>



| <span data-ttu-id="097da-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="097da-179">Requirement</span></span> | <span data-ttu-id="097da-180">Wert</span><span class="sxs-lookup"><span data-stu-id="097da-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="097da-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="097da-181">Minimum supported client</span></span><br/> | <span data-ttu-id="097da-182">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="097da-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="097da-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="097da-183">Minimum supported server</span></span><br/> | <span data-ttu-id="097da-184">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="097da-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="097da-185">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="097da-185">End of client support</span></span><br/>    | <span data-ttu-id="097da-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="097da-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="097da-187">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="097da-187">End of server support</span></span><br/>    | <span data-ttu-id="097da-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="097da-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="097da-189">Header</span><span class="sxs-lookup"><span data-stu-id="097da-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="097da-190"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="097da-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="097da-191">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="097da-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="097da-192"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="097da-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="097da-193">DLL</span><span class="sxs-lookup"><span data-stu-id="097da-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="097da-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="097da-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="097da-195">IID</span><span class="sxs-lookup"><span data-stu-id="097da-195">IID</span></span><br/>                      | <span data-ttu-id="097da-196">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="097da-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="097da-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="097da-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097da-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="097da-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="097da-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="097da-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
