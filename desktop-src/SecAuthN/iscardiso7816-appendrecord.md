---
description: Die appendrecord-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der entweder einen Datensatz an das Ende einer linear strukturierten elementaren Datei (EF) anfügt oder die Datensatznummer 1 in einer zyklisch strukturierten elementaren Datei schreibt.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'ISCardISO7816:: appendrecord-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215108"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="a1a8a-103">ISCardISO7816:: appendrecord-Methode</span><span class="sxs-lookup"><span data-stu-id="a1a8a-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="a1a8a-104">\[Die **appendrecord** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1a8a-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a1a8a-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a1a8a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a1a8a-107">Die **appendrecord** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der entweder einen Datensatz an das Ende einer linear strukturierten elementaren Datei (EF) anfügt oder die Datensatznummer 1 in einer zyklisch strukturierten elementaren Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1a8a-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a1a8a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1a8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a8a-110">*ByRef STRG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1a8a-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a8a-111">Identifiziert die anzufügende elementare Datei.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="a1a8a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a8a-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="a1a8a-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1a8a-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="a1a8a-114"><dt>**Aktuelles EF**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="a1a8a-115">Bitposition: 00000000</span><span class="sxs-lookup"><span data-stu-id="a1a8a-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="a1a8a-116"><dt>**Kurze EF-ID**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="a1a8a-117">Bitposition: xxxxx000</span><span class="sxs-lookup"><span data-stu-id="a1a8a-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="a1a8a-118"><dt>**Reserviert**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="a1a8a-119">Bitposition: xxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="a1a8a-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1a8a-120">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1a8a-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a8a-121">Ein Zeiger auf die Daten, die an die Datei angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="a1a8a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a8a-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="a1a8a-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1a8a-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="a1a8a-124"><dt>**TN**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="a1a8a-125">1 Byte</span><span class="sxs-lookup"><span data-stu-id="a1a8a-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="a1a8a-126"><dt>**Ln**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="a1a8a-127">1 oder 3 Bytes</span><span class="sxs-lookup"><span data-stu-id="a1a8a-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="a1a8a-128"><dt>**Vorrats**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="a1a8a-129">LN bytes</span><span class="sxs-lookup"><span data-stu-id="a1a8a-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="a1a8a-130">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1a8a-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a8a-131">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a1a8a-132">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a1a8a-133">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mithilfe des *ppcmd* -Zeigers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a8a-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1a8a-134">Return value</span></span>

<span data-ttu-id="a1a8a-135">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a1a8a-136">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a1a8a-136">Return code</span></span>                                                                                   | <span data-ttu-id="a1a8a-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1a8a-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a1a8a-138"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a1a8a-139">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a1a8a-140"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a1a8a-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a1a8a-142"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a1a8a-143">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a1a8a-144"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a1a8a-145">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a1a8a-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1a8a-146">Remarks</span></span>

<span data-ttu-id="a1a8a-147">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen des Lesevorgangs der elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="a1a8a-148">Wenn zum Zeitpunkt der Ausgabe dieses Befehls eine andere elementare Datei ausgewählt ist, wird Sie möglicherweise ohne Identifikation der aktuell ausgewählten Datei verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="a1a8a-149">Elementare Dateien ohne Daten Satzstruktur können nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="a1a8a-150">Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="a1a8a-151">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="a1a8a-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a1a8a-152">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a1a8a-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a1a8a-153">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a1a8a-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a8a-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1a8a-154">Requirements</span></span>



| <span data-ttu-id="a1a8a-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1a8a-155">Requirement</span></span> | <span data-ttu-id="a1a8a-156">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a8a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a8a-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1a8a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a8a-158">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1a8a-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a1a8a-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1a8a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a8a-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1a8a-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1a8a-161">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a1a8a-161">End of client support</span></span><br/>    | <span data-ttu-id="a1a8a-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1a8a-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a1a8a-163">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a1a8a-163">End of server support</span></span><br/>    | <span data-ttu-id="a1a8a-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1a8a-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a1a8a-165">Header</span><span class="sxs-lookup"><span data-stu-id="a1a8a-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1a8a-166"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1a8a-167">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a1a8a-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1a8a-168"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1a8a-169">DLL</span><span class="sxs-lookup"><span data-stu-id="a1a8a-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1a8a-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8a-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1a8a-171">IID</span><span class="sxs-lookup"><span data-stu-id="a1a8a-171">IID</span></span><br/>                      | <span data-ttu-id="a1a8a-172">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="a1a8a-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a1a8a-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1a8a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a8a-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a1a8a-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="a1a8a-175">**Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="a1a8a-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="a1a8a-176">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="a1a8a-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="a1a8a-177">**Beschreibecord**</span><span class="sxs-lookup"><span data-stu-id="a1a8a-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
