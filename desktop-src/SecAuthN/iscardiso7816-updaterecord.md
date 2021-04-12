---
description: Die UpdateRecord-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der einen bestimmten Datensatz mit den Bits aktualisiert, die im APDU-Befehl angegeben sind.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'ISCardISO7816:: UpdateRecord-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216212"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="f4b2e-103">ISCardISO7816:: UpdateRecord-Methode</span><span class="sxs-lookup"><span data-stu-id="f4b2e-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="f4b2e-104">\[Die **UpdateRecord** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f4b2e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f4b2e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f4b2e-107">Die **UpdateRecord** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der einen bestimmten Datensatz mit den Bits aktualisiert, die im APDU-Befehl angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="f4b2e-108">Bei der Verwendung der aktuellen Daten Satz Adressierung legt der Befehl den Datensatz-Zeiger auf den erfolgreich aktualisierten Datensatz fest.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f4b2e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4b2e-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="f4b2e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4b2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4b2e-111">*byrecordid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4b2e-112">P1-Wert:</span><span class="sxs-lookup"><span data-stu-id="f4b2e-112">P1 value:</span></span>

<span data-ttu-id="f4b2e-113">P1 = 00 legt den aktuellen Datensatz fest.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="f4b2e-114">P1! = ' 00 ' ist die Nummer des angegebenen Datensatzes</span><span class="sxs-lookup"><span data-stu-id="f4b2e-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="f4b2e-115">*ByRef STRG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4b2e-116">Codieren des Verweis Steuer Elements P2:</span><span class="sxs-lookup"><span data-stu-id="f4b2e-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="f4b2e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f4b2e-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="f4b2e-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f4b2e-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="f4b2e-119"><dt>**Aktuelles EF**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="f4b2e-120">Bitposition: 00000---</span><span class="sxs-lookup"><span data-stu-id="f4b2e-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="f4b2e-121">Aktuell ausgewähltes EF.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="f4b2e-122"><dt>**Kurze EF-ID**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="f4b2e-123">Bitposition: XXXXX---</span><span class="sxs-lookup"><span data-stu-id="f4b2e-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="f4b2e-124">Kurzer EF-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="f4b2e-125"><dt>**Erster Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="f4b2e-126">Bitposition:-----000</span><span class="sxs-lookup"><span data-stu-id="f4b2e-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="f4b2e-127"><dt>**Letzter Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="f4b2e-128">Bitposition:-----001</span><span class="sxs-lookup"><span data-stu-id="f4b2e-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="f4b2e-129"><dt>**Nächster Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="f4b2e-130">Bitposition:-----010</span><span class="sxs-lookup"><span data-stu-id="f4b2e-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="f4b2e-131"><dt>**Vorheriger Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="f4b2e-132">Bitposition:-----011</span><span class="sxs-lookup"><span data-stu-id="f4b2e-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="f4b2e-133"><dt>**Datensatz \# in P1**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="f4b2e-134">Bitposition:-----100</span><span class="sxs-lookup"><span data-stu-id="f4b2e-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="f4b2e-135">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4b2e-136">Zeiger auf den zu aktualisierenden Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="f4b2e-137">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4b2e-138">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="f4b2e-139">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="f4b2e-140">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4b2e-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4b2e-141">Return value</span></span>

<span data-ttu-id="f4b2e-142">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f4b2e-143">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f4b2e-143">Return code</span></span>                                                                                   | <span data-ttu-id="f4b2e-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4b2e-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f4b2e-145"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f4b2e-146">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f4b2e-147"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f4b2e-148">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f4b2e-149"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f4b2e-150">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="f4b2e-151"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f4b2e-152">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f4b2e-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4b2e-153">Remarks</span></span>

<span data-ttu-id="f4b2e-154">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="f4b2e-155">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="f4b2e-156">Wenn derzeit eine andere elementare Datei zum Zeitpunkt der Ausgabe dieses Befehls ausgewählt ist, kann dieser Befehl ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="f4b2e-157">Wenn der konstruierte Befehl für eine lineare oder zyklische strukturierte elementare Datei gilt, wird er abgebrochen, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="f4b2e-158">Wenn der Befehl auf eine strukturierte elementare Datei für eine lineare Variable angewendet wird, kann er ausgeführt werden, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="f4b2e-159">Die "Previous"-Option des Befehls (P2 = xxxxx011), der auf eine zyklische Datei angewendet wird, hat das gleiche Verhalten wie ein Befehl, der von [**appendrecord**](iscardiso7816-appendrecord.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="f4b2e-160">Elementare Dateien ohne Daten Satzstruktur können nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="f4b2e-161">Der konstruierte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="f4b2e-162">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="f4b2e-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="f4b2e-163">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f4b2e-164">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f4b2e-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b2e-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4b2e-165">Requirements</span></span>



| <span data-ttu-id="f4b2e-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4b2e-166">Requirement</span></span> | <span data-ttu-id="f4b2e-167">Wert</span><span class="sxs-lookup"><span data-stu-id="f4b2e-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b2e-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4b2e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b2e-169">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f4b2e-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4b2e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b2e-171">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4b2e-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4b2e-172">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f4b2e-172">End of client support</span></span><br/>    | <span data-ttu-id="f4b2e-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4b2e-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f4b2e-174">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f4b2e-174">End of server support</span></span><br/>    | <span data-ttu-id="f4b2e-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4b2e-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f4b2e-176">Header</span><span class="sxs-lookup"><span data-stu-id="f4b2e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4b2e-177"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4b2e-178">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f4b2e-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4b2e-179"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f4b2e-180">DLL</span><span class="sxs-lookup"><span data-stu-id="f4b2e-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4b2e-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4b2e-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4b2e-182">IID</span><span class="sxs-lookup"><span data-stu-id="f4b2e-182">IID</span></span><br/>                      | <span data-ttu-id="f4b2e-183">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="f4b2e-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f4b2e-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4b2e-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4b2e-185">**Appenddatensatz**</span><span class="sxs-lookup"><span data-stu-id="f4b2e-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="f4b2e-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="f4b2e-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="f4b2e-187">**Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="f4b2e-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="f4b2e-188">**Beschreibecord**</span><span class="sxs-lookup"><span data-stu-id="f4b2e-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
