---
description: Die Read Record-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der entweder den Inhalt der angegebenen Datensätze oder den Anfangsteil eines Datensatzes einer elementaren Datei liest.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816:: Read Record-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042224"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="7086e-103">ISCardISO7816:: Read Record-Methode</span><span class="sxs-lookup"><span data-stu-id="7086e-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="7086e-104">\[Die Methode "read **Record** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7086e-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7086e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7086e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7086e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7086e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7086e-107">Die Read **Record** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der entweder den Inhalt der angegebenen Datensätze oder den Anfangsteil eines Datensatzes einer elementaren Datei liest.</span><span class="sxs-lookup"><span data-stu-id="7086e-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7086e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7086e-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="7086e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7086e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7086e-110">*byrecordid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7086e-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7086e-111">Datensatznummer oder ID des ersten zu lesenden Datensatzes (00 gibt den aktuellen Datensatz an).</span><span class="sxs-lookup"><span data-stu-id="7086e-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="7086e-112">*ByRef STRG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7086e-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7086e-113">Codieren des Verweis Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="7086e-113">Coding of the reference control.</span></span>



| <span data-ttu-id="7086e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7086e-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="7086e-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7086e-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="7086e-116"><dt>**Aktuelles EF**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="7086e-117">Bitposition: 00000---</span><span class="sxs-lookup"><span data-stu-id="7086e-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="7086e-118">Aktuell ausgewähltes EF.</span><span class="sxs-lookup"><span data-stu-id="7086e-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="7086e-119"><dt>**Kurze EF-ID**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="7086e-120">Bitposition: XXXXX---</span><span class="sxs-lookup"><span data-stu-id="7086e-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="7086e-121">Kurzer EF-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7086e-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="7086e-122"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="7086e-123">Bitposition: 11111---</span><span class="sxs-lookup"><span data-stu-id="7086e-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="7086e-124"><dt>**Aufnahme \#**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="7086e-125">Bitposition:-----1xx</span><span class="sxs-lookup"><span data-stu-id="7086e-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="7086e-126">Verwendung der Datensatznummer in P1.</span><span class="sxs-lookup"><span data-stu-id="7086e-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="7086e-127"><dt>**Datensatz lesen**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="7086e-128">Bitposition:-----100</span><span class="sxs-lookup"><span data-stu-id="7086e-128">Bit position: -----100</span></span><br/> <span data-ttu-id="7086e-129">Lesen Sie den Datensatz P1.</span><span class="sxs-lookup"><span data-stu-id="7086e-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="7086e-130"><dt>**Bis zum letzten**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="7086e-131">Bitposition:-----101</span><span class="sxs-lookup"><span data-stu-id="7086e-131">Bit position: -----101</span></span><br/> <span data-ttu-id="7086e-132">Lesen Sie alle Datensätze von P1 bis zum letzten.</span><span class="sxs-lookup"><span data-stu-id="7086e-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="7086e-133"><dt>**Bis zu P1**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="7086e-134">Bitposition:-----110</span><span class="sxs-lookup"><span data-stu-id="7086e-134">Bit position: -----110</span></span><br/> <span data-ttu-id="7086e-135">Lesen Sie alle Datensätze von der letzten bis zu P1.</span><span class="sxs-lookup"><span data-stu-id="7086e-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="7086e-136"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="7086e-137">Bitposition:-----111</span><span class="sxs-lookup"><span data-stu-id="7086e-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="7086e-138"><dt>**Datensatz-ID**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="7086e-139">Bitposition:-----0xx</span><span class="sxs-lookup"><span data-stu-id="7086e-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="7086e-140">Verwendung der Datensatznummer in P1.</span><span class="sxs-lookup"><span data-stu-id="7086e-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="7086e-141"><dt>**Zuerst auftreten**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="7086e-142">Bitposition:-----000</span><span class="sxs-lookup"><span data-stu-id="7086e-142">Bit position: -----000</span></span><br/> <span data-ttu-id="7086e-143">Lesen Sie das erste Vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7086e-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="7086e-144"><dt>**Letztes vorkommen**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="7086e-145">Bitposition:-----001</span><span class="sxs-lookup"><span data-stu-id="7086e-145">Bit position: -----001</span></span><br/> <span data-ttu-id="7086e-146">Letztes vorkommen lesen.</span><span class="sxs-lookup"><span data-stu-id="7086e-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="7086e-147"><dt>**Nächstes Vorkommen**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="7086e-148">Bitposition:-----010</span><span class="sxs-lookup"><span data-stu-id="7086e-148">Bit position: -----010</span></span><br/> <span data-ttu-id="7086e-149">Nächste Vorkommen lesen.</span><span class="sxs-lookup"><span data-stu-id="7086e-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="7086e-150"><dt>**Vorherige**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="7086e-151">Bitposition:-----011</span><span class="sxs-lookup"><span data-stu-id="7086e-151">Bit position: -----011</span></span><br/> <span data-ttu-id="7086e-152">Vorheriges Vorkommen lesen.</span><span class="sxs-lookup"><span data-stu-id="7086e-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="7086e-153"><dt>**Geheimen**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="7086e-154">Bitposition:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="7086e-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="7086e-155">*lbytestoread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7086e-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7086e-156">Anzahl der Bytes, die aus dem transparenten EF gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7086e-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="7086e-157">Wenn das Feld Le nur Nullen enthält, sollte der Befehl je nach b3b2b1 von P2 und innerhalb des Limits von 256 für kurze Länge oder 65536 für erweiterte Länge entweder den einzelnen angeforderten Datensatz oder die angeforderte Sequenz von Datensätzen vollständig lesen.</span><span class="sxs-lookup"><span data-stu-id="7086e-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="7086e-158">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7086e-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7086e-159">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="7086e-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="7086e-160">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="7086e-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="7086e-161">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7086e-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7086e-162">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7086e-162">Return value</span></span>

<span data-ttu-id="7086e-163">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7086e-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7086e-164">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7086e-164">Return code</span></span>                                                                                   | <span data-ttu-id="7086e-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7086e-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7086e-166"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7086e-167">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7086e-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7086e-168"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7086e-169">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="7086e-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="7086e-170"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7086e-171">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7086e-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="7086e-172"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7086e-173">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7086e-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7086e-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7086e-174">Remarks</span></span>

<span data-ttu-id="7086e-175">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu lesenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="7086e-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="7086e-176">Wenn derzeit eine andere elementare Datei zum Zeitpunkt der Ausgabe dieses Befehls ausgewählt ist, kann Sie ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7086e-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="7086e-177">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7086e-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="7086e-178">Elementare Dateien ohne Daten Satzstruktur können nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="7086e-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="7086e-179">Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7086e-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="7086e-180">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="7086e-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="7086e-181">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7086e-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7086e-182">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7086e-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7086e-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7086e-183">Requirements</span></span>



| <span data-ttu-id="7086e-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7086e-184">Requirement</span></span> | <span data-ttu-id="7086e-185">Wert</span><span class="sxs-lookup"><span data-stu-id="7086e-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7086e-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7086e-186">Minimum supported client</span></span><br/> | <span data-ttu-id="7086e-187">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7086e-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7086e-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7086e-188">Minimum supported server</span></span><br/> | <span data-ttu-id="7086e-189">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7086e-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7086e-190">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7086e-190">End of client support</span></span><br/>    | <span data-ttu-id="7086e-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7086e-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7086e-192">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7086e-192">End of server support</span></span><br/>    | <span data-ttu-id="7086e-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7086e-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7086e-194">Header</span><span class="sxs-lookup"><span data-stu-id="7086e-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="7086e-195"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7086e-196">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7086e-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="7086e-197"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7086e-198">DLL</span><span class="sxs-lookup"><span data-stu-id="7086e-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7086e-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7086e-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7086e-200">IID</span><span class="sxs-lookup"><span data-stu-id="7086e-200">IID</span></span><br/>                      | <span data-ttu-id="7086e-201">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="7086e-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7086e-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7086e-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7086e-203">**Appenddatensatz**</span><span class="sxs-lookup"><span data-stu-id="7086e-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="7086e-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="7086e-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="7086e-205">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="7086e-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="7086e-206">**Beschreibecord**</span><span class="sxs-lookup"><span data-stu-id="7086e-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
