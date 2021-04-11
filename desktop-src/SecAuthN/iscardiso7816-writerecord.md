---
description: Erstellt einen APDU-Befehl, der einen der aufgelisteten Vorgänge initiiert.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816:: beschreiterecord-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128292"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="7430c-103">ISCardISO7816:: beschreiterecord-Methode</span><span class="sxs-lookup"><span data-stu-id="7430c-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="7430c-104">\[Die Methode " **beschreiterecord** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7430c-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7430c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7430c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7430c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7430c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7430c-107">Die **beschreiterecord** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der einen der folgenden Vorgänge initiiert:</span><span class="sxs-lookup"><span data-stu-id="7430c-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="7430c-108">Der einmal Schreibvorgang eines Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="7430c-108">The write once of a record.</span></span>
-   <span data-ttu-id="7430c-109">Das logische **or** der Daten Bytes eines Datensatzes, der bereits in der Karte vorhanden ist, mit den Daten Bytes des Datensatzes, der im Befehl APDU angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7430c-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="7430c-110">Das logische und der Daten Bytes eines Datensatzes, die bereits in der Karte vorhanden sind, mit den Daten Bytes des Datensatzes, der im Befehl APDU angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7430c-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="7430c-111">Wenn im Daten Codierungs Byte keine Angabe angegeben ist, gilt das logische OR-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="7430c-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="7430c-112">Bei der Verwendung der aktuellen Daten Satz Adressierung legt der Befehl den Datensatz-Zeiger auf den erfolgreich aktualisierten Datensatz fest.</span><span class="sxs-lookup"><span data-stu-id="7430c-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7430c-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="7430c-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="7430c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7430c-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7430c-115">*byrecordid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7430c-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7430c-116">Datensatz-ID.</span><span class="sxs-lookup"><span data-stu-id="7430c-116">Record identification.</span></span> <span data-ttu-id="7430c-117">Dies ist der P1-Wert:</span><span class="sxs-lookup"><span data-stu-id="7430c-117">This is the P1 value:</span></span>

<span data-ttu-id="7430c-118">P1 = ' 00 ' gibt den aktuellen Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="7430c-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="7430c-119">P1! = ' 00 ' ist die Nummer des angegebenen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="7430c-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="7430c-120">*ByRef STRG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7430c-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7430c-121">Codieren des Verweis Steuer Elements P2.</span><span class="sxs-lookup"><span data-stu-id="7430c-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="7430c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7430c-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="7430c-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7430c-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="7430c-124"><dt>**Aktuelles EF**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="7430c-125">Bitposition: 00000---</span><span class="sxs-lookup"><span data-stu-id="7430c-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="7430c-126">Aktuell ausgewähltes EF.</span><span class="sxs-lookup"><span data-stu-id="7430c-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="7430c-127"><dt>**Kurze EF-ID**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="7430c-128">Bitposition: XXXXX---</span><span class="sxs-lookup"><span data-stu-id="7430c-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="7430c-129">Kurzer EF-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7430c-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="7430c-130"><dt>**Erster Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="7430c-131">Bitposition:-----000</span><span class="sxs-lookup"><span data-stu-id="7430c-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="7430c-132"><dt>**Letzter Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="7430c-133">Bitposition:-----001</span><span class="sxs-lookup"><span data-stu-id="7430c-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="7430c-134"><dt>**Nächster Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="7430c-135">Bitposition:-----010</span><span class="sxs-lookup"><span data-stu-id="7430c-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="7430c-136"><dt>**Vorheriger Datensatz**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="7430c-137">Bitposition:-----011</span><span class="sxs-lookup"><span data-stu-id="7430c-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="7430c-138"><dt>**Datensatz \# in P1**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="7430c-139">Bitposition:-----100</span><span class="sxs-lookup"><span data-stu-id="7430c-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="7430c-140">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7430c-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7430c-141">Zeiger auf den zu schreibenden Datensatz.</span><span class="sxs-lookup"><span data-stu-id="7430c-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="7430c-142">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7430c-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7430c-143">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="7430c-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="7430c-144">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="7430c-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="7430c-145">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7430c-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7430c-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7430c-146">Return value</span></span>

<span data-ttu-id="7430c-147">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7430c-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7430c-148">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7430c-148">Return code</span></span>                                                                                   | <span data-ttu-id="7430c-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7430c-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7430c-150"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7430c-151">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7430c-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7430c-152"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7430c-153">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="7430c-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="7430c-154"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7430c-155">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7430c-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="7430c-156"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7430c-157">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7430c-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7430c-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7430c-158">Remarks</span></span>

<span data-ttu-id="7430c-159">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="7430c-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="7430c-160">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7430c-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="7430c-161">Wenn derzeit eine andere elementare Datei zum Zeitpunkt der Ausgabe dieses Befehls ausgewählt ist, kann dieser Befehl ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7430c-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="7430c-162">Wenn der gekapselte Befehl für eine lineare oder zyklische strukturierte elementare Datei gilt, wird er abgebrochen, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.</span><span class="sxs-lookup"><span data-stu-id="7430c-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="7430c-163">Wenn Sie sich auf eine strukturierte elementare Datei für eine lineare Variable bezieht, wird Sie möglicherweise ausgeführt, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.</span><span class="sxs-lookup"><span data-stu-id="7430c-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="7430c-164">Wenn P2 = xxxxx011 und die elementare Datei zyklisch sind, weist dieser Befehl das gleiche Verhalten auf wie bei einem mit [**appendrecord**](iscardiso7816-appendrecord.md)erstellten Befehl.</span><span class="sxs-lookup"><span data-stu-id="7430c-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="7430c-165">Auf elementare Dateien ohne eine Daten Satzstruktur kann nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7430c-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="7430c-166">Der konstruierte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7430c-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="7430c-167">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="7430c-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="7430c-168">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7430c-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7430c-169">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7430c-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7430c-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7430c-170">Requirements</span></span>



| <span data-ttu-id="7430c-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7430c-171">Requirement</span></span> | <span data-ttu-id="7430c-172">Wert</span><span class="sxs-lookup"><span data-stu-id="7430c-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7430c-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7430c-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7430c-174">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7430c-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7430c-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7430c-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7430c-176">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7430c-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7430c-177">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7430c-177">End of client support</span></span><br/>    | <span data-ttu-id="7430c-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7430c-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7430c-179">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7430c-179">End of server support</span></span><br/>    | <span data-ttu-id="7430c-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7430c-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7430c-181">Header</span><span class="sxs-lookup"><span data-stu-id="7430c-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="7430c-182"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7430c-183">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7430c-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="7430c-184"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7430c-185">DLL</span><span class="sxs-lookup"><span data-stu-id="7430c-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7430c-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7430c-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7430c-187">IID</span><span class="sxs-lookup"><span data-stu-id="7430c-187">IID</span></span><br/>                      | <span data-ttu-id="7430c-188">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="7430c-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7430c-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7430c-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7430c-190">**Appenddatensatz**</span><span class="sxs-lookup"><span data-stu-id="7430c-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="7430c-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="7430c-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="7430c-192">**Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="7430c-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="7430c-193">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="7430c-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
