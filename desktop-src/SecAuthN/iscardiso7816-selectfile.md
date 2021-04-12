---
description: Die selectfile-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), mit dem eine aktuelle elementare Datei innerhalb eines logischen Kanals festgelegt wird. Nachfolgende Befehle können implizit über den logischen Kanal auf die aktuelle Datei verweisen.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816:: selectfile-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216211"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="46111-104">ISCardISO7816:: selectfile-Methode</span><span class="sxs-lookup"><span data-stu-id="46111-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="46111-105">\[Die **selectfile** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="46111-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="46111-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46111-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="46111-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="46111-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="46111-108">Die **selectfile** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), mit dem eine aktuelle elementare Datei innerhalb eines logischen Kanals festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="46111-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="46111-109">Nachfolgende Befehle können implizit über den logischen Kanal auf die aktuelle Datei verweisen.</span><span class="sxs-lookup"><span data-stu-id="46111-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="46111-110">Wenn Sie ein Verzeichnis (DF) im Kartendatei Speicher auswählen, d. –. das Stammverzeichnis (MF) des Dateispeicher –, wird es zur aktuellen DF.</span><span class="sxs-lookup"><span data-stu-id="46111-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="46111-111">Nach einer solchen Auswahl kann über diesen logischen Kanal auf eine implizite aktuelle elementare Datei verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="46111-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="46111-112">Wenn Sie eine elementare Datei auswählen, werden die ausgewählte Datei und deren übergeordnetes Element als aktuelle Dateien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="46111-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="46111-113">Nachdem die Antwort zurückgesetzt wurde, wird der MF implizit über den logischen Standard Kanal ausgewählt, es sei denn, er wurde in den Verlaufs Bytes oder in der ursprünglichen Daten Zeichenfolge anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="46111-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="46111-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="46111-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="46111-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="46111-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46111-116">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46111-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46111-117">Auswahl Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="46111-117">Selection control.</span></span>



| <span data-ttu-id="46111-118">P1 (oberes Byte in Word): 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="46111-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="46111-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="46111-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="46111-120"><dt>**000000xx**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="46111-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="46111-121">Datei-ID auswählen</span><span class="sxs-lookup"><span data-stu-id="46111-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="46111-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="46111-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="46111-123">EF, DF oder MF</span><span class="sxs-lookup"><span data-stu-id="46111-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="46111-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="46111-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="46111-125">Untergeordnete DF</span><span class="sxs-lookup"><span data-stu-id="46111-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="46111-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="46111-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="46111-127">EF unter DF</span><span class="sxs-lookup"><span data-stu-id="46111-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="46111-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="46111-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="46111-129">Übergeordnete DF der aktuellen DF</span><span class="sxs-lookup"><span data-stu-id="46111-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="46111-130">Wenn P1 = 00 ist, weiß die Karte entweder aufgrund einer bestimmten Codierung der Datei-ID oder aufgrund des Kontexts der Ausführung des Befehls, wenn die ausgewählte Datei das MF, ein DF oder EF ist.</span><span class="sxs-lookup"><span data-stu-id="46111-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="46111-131">Wenn P1-P2 = 0000, wenn eine Datei-ID bereitgestellt wird, wird Sie in den folgenden Umgebungen eindeutig sein:</span><span class="sxs-lookup"><span data-stu-id="46111-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="46111-132">Unmittelbare untergeordnete Elemente der aktuellen DF</span><span class="sxs-lookup"><span data-stu-id="46111-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="46111-133">Übergeordnete DF</span><span class="sxs-lookup"><span data-stu-id="46111-133">Parent DF</span></span>
-   <span data-ttu-id="46111-134">Unmittelbare untergeordnete Elemente der übergeordneten DF</span><span class="sxs-lookup"><span data-stu-id="46111-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="46111-135">Wenn P1-P2 = 0000 und das Datenfeld leer oder gleich 3f00 ist, wählen Sie den MF aus.</span><span class="sxs-lookup"><span data-stu-id="46111-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="46111-136">Bei P1 = 04 ist das Datenfeld ein DF-Name, der möglicherweise rechts abgeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="46111-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="46111-137">Wenn dies unterstützt wird, müssen nachfolgende Befehle desselben Datenfelds DFS auswählen, deren Namen mit dem Datenfeld übereinstimmen (d. h. mit dem Feld "Befehlsdaten" beginnen).</span><span class="sxs-lookup"><span data-stu-id="46111-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="46111-138">Wenn die Karte den Befehl mit einem leeren Datenfeld akzeptiert, können alle oder eine Teilmenge der DFS nacheinander ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="46111-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="46111-139">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46111-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46111-140">Auswahl Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="46111-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="46111-141">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46111-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46111-142">Daten für den Vorgang bei Bedarf. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="46111-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="46111-143">Zu den Datentypen, die in diesem Parameter übergeben werden, gehören:</span><span class="sxs-lookup"><span data-stu-id="46111-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="46111-144">Datei-ID</span><span class="sxs-lookup"><span data-stu-id="46111-144">file ID</span></span>
-   <span data-ttu-id="46111-145">Pfad aus dem MF</span><span class="sxs-lookup"><span data-stu-id="46111-145">path from the MF</span></span>
-   <span data-ttu-id="46111-146">Pfad der aktuellen DF</span><span class="sxs-lookup"><span data-stu-id="46111-146">path from the current DF</span></span>
-   <span data-ttu-id="46111-147">Name der DF</span><span class="sxs-lookup"><span data-stu-id="46111-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="46111-148">*lbytestoread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46111-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46111-149">Leer (d. h. 0) oder die maximale Länge der Daten, die als Antwort erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="46111-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="46111-150">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="46111-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46111-151">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="46111-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="46111-152">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="46111-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="46111-153">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46111-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46111-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46111-154">Return value</span></span>

<span data-ttu-id="46111-155">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="46111-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="46111-156">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="46111-156">Return code</span></span>                                                                                   | <span data-ttu-id="46111-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46111-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="46111-158"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46111-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="46111-159">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="46111-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="46111-160"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="46111-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="46111-161">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="46111-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="46111-162"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="46111-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="46111-163">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="46111-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="46111-164"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="46111-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="46111-165">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="46111-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="46111-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46111-166">Remarks</span></span>

<span data-ttu-id="46111-167">Sofern nicht anders angegeben, ändert die korrekte Ausführung des gekapselten Befehls den Sicherheitsstatus gemäß den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="46111-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="46111-168">Wenn die aktuelle elementare Datei geändert wird oder wenn keine aktuelle elementare Datei vorhanden ist, geht der für eine frühere aktuelle elementare Datei spezifische Sicherheitsstatus verloren.</span><span class="sxs-lookup"><span data-stu-id="46111-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="46111-169">Wenn das aktuelle Dateispeicher Verzeichnis (DF) ein Nachfolger von ist oder mit dem früheren aktuellen DF identisch ist, geht der Sicherheitsstatus, der für die vorherige aktuelle DF spezifisch ist, verloren.</span><span class="sxs-lookup"><span data-stu-id="46111-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="46111-170">Der Sicherheitsstatus, der für alle gemeinsamen Vorgänger der vorherigen und neuen aktuellen DF gilt, wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="46111-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="46111-171">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="46111-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="46111-172">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="46111-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="46111-173">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="46111-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46111-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46111-174">Requirements</span></span>



| <span data-ttu-id="46111-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46111-175">Requirement</span></span> | <span data-ttu-id="46111-176">Wert</span><span class="sxs-lookup"><span data-stu-id="46111-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46111-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46111-177">Minimum supported client</span></span><br/> | <span data-ttu-id="46111-178">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46111-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="46111-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46111-179">Minimum supported server</span></span><br/> | <span data-ttu-id="46111-180">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46111-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46111-181">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="46111-181">End of client support</span></span><br/>    | <span data-ttu-id="46111-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46111-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="46111-183">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="46111-183">End of server support</span></span><br/>    | <span data-ttu-id="46111-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46111-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="46111-185">Header</span><span class="sxs-lookup"><span data-stu-id="46111-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="46111-186"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="46111-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="46111-187">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="46111-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="46111-188"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46111-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46111-189">DLL</span><span class="sxs-lookup"><span data-stu-id="46111-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46111-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46111-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="46111-191">IID</span><span class="sxs-lookup"><span data-stu-id="46111-191">IID</span></span><br/>                      | <span data-ttu-id="46111-192">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="46111-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="46111-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46111-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46111-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="46111-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
