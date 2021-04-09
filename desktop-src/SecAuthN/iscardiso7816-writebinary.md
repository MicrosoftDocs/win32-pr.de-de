---
description: Die Methode "Write Binary" erstellt einen APDU-Befehl (Application Protocol Data Unit), der binäre Werte in eine elementare Datei schreibt.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816:: Beschreib tebinary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958701"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="039ca-103">ISCardISO7816:: Beschreib tebinary-Methode</span><span class="sxs-lookup"><span data-stu-id="039ca-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="039ca-104">\[Die Methode " **Write Binary** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="039ca-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="039ca-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="039ca-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="039ca-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="039ca-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="039ca-107">Die Methode " **Write Binary** " erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der binäre Werte in eine elementare Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="039ca-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="039ca-108">Abhängig von den Dateiattributen führt der Befehl einen der folgenden Vorgänge aus:</span><span class="sxs-lookup"><span data-stu-id="039ca-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="039ca-109">Das logische OR der Bits, die bereits in der Karte vorhanden sind, mit den Bits, die im APDU-Befehl angegeben sind (logischer Lösch Zustand der Bits der Datei ist 0).</span><span class="sxs-lookup"><span data-stu-id="039ca-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="039ca-110">Das logische und der Bits, die bereits in der Karte vorhanden sind, mit den Bits, die im Befehl APDU angegeben sind (logischer Lösch Zustand der Bits der Datei ist 1).</span><span class="sxs-lookup"><span data-stu-id="039ca-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="039ca-111">Der einmalige Schreibvorgang in der Karte der Bits, die im Befehl APDU angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="039ca-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="039ca-112">Wenn im Daten Codierungs Byte keine Angabe angegeben ist, gilt das logische OR-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="039ca-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="039ca-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="039ca-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="039ca-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="039ca-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="039ca-115">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="039ca-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="039ca-116">Offset am Schreib Speicherort vom Anfang der Binärdatei (EF).</span><span class="sxs-lookup"><span data-stu-id="039ca-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="039ca-117">Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, die Größe von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="039ca-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="039ca-118">Wenn "B8 = 0" in P1 \| \| ist, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="039ca-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="039ca-119">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="039ca-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="039ca-120">Offset am Schreib Speicherort vom Anfang der Binärdatei (EF).</span><span class="sxs-lookup"><span data-stu-id="039ca-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="039ca-121">Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, die Größe von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="039ca-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="039ca-122">Wenn "B8 = 0" in P1 \| \| ist, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="039ca-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="039ca-123">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="039ca-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="039ca-124">Ein Zeiger auf die Zeichenfolge der zu schreibenden Dateneinheiten.</span><span class="sxs-lookup"><span data-stu-id="039ca-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="039ca-125">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="039ca-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="039ca-126">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="039ca-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="039ca-127">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="039ca-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="039ca-128">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="039ca-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="039ca-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="039ca-129">Return value</span></span>

<span data-ttu-id="039ca-130">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="039ca-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="039ca-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="039ca-131">Return code</span></span>                                                                                   | <span data-ttu-id="039ca-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="039ca-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="039ca-133"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="039ca-134">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="039ca-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="039ca-135"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="039ca-136">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="039ca-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="039ca-137"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="039ca-138">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="039ca-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="039ca-139"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="039ca-140">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="039ca-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="039ca-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="039ca-141">Remarks</span></span>

<span data-ttu-id="039ca-142">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="039ca-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="039ca-143">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="039ca-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="039ca-144">Wenn ein Schreib binärer Vorgang auf eine Dateneinheit eines einmaligen Schreibvorgangs von EF angewendet wurde, werden alle weiteren Schreibvorgänge, die auf diese Dateneinheit verweisen, abgebrochen, wenn sich der Inhalt der Dateneinheit oder der logische Lösch Status Indikator (sofern vorhanden), der an diese Dateneinheit angefügt ist, vom logischen gelöschten Zustand unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="039ca-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="039ca-145">Auf elementare Dateien ohne transparente Struktur kann nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="039ca-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="039ca-146">Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="039ca-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="039ca-147">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="039ca-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="039ca-148">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="039ca-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="039ca-149">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="039ca-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="039ca-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="039ca-150">Requirements</span></span>



| <span data-ttu-id="039ca-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="039ca-151">Requirement</span></span> | <span data-ttu-id="039ca-152">Wert</span><span class="sxs-lookup"><span data-stu-id="039ca-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="039ca-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="039ca-153">Minimum supported client</span></span><br/> | <span data-ttu-id="039ca-154">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="039ca-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="039ca-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="039ca-155">Minimum supported server</span></span><br/> | <span data-ttu-id="039ca-156">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="039ca-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="039ca-157">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="039ca-157">End of client support</span></span><br/>    | <span data-ttu-id="039ca-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="039ca-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="039ca-159">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="039ca-159">End of server support</span></span><br/>    | <span data-ttu-id="039ca-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="039ca-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="039ca-161">Header</span><span class="sxs-lookup"><span data-stu-id="039ca-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="039ca-162"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="039ca-163">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="039ca-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="039ca-164"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="039ca-165">DLL</span><span class="sxs-lookup"><span data-stu-id="039ca-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="039ca-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="039ca-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="039ca-167">IID</span><span class="sxs-lookup"><span data-stu-id="039ca-167">IID</span></span><br/>                      | <span data-ttu-id="039ca-168">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="039ca-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="039ca-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="039ca-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039ca-170">**Erasebinary**</span><span class="sxs-lookup"><span data-stu-id="039ca-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="039ca-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="039ca-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="039ca-172">**"Read Binary"**</span><span class="sxs-lookup"><span data-stu-id="039ca-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="039ca-173">**Updatebinary**</span><span class="sxs-lookup"><span data-stu-id="039ca-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
