---
description: Die updatebinary-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), mit dem die Bits, die in einer elementaren Datei vorhanden sind, mit den im APDU-Befehl angegebenen Bits aktualisiert werden.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'ISCardISO7816:: updatebinary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348679"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="86c2d-103">ISCardISO7816:: updatebinary-Methode</span><span class="sxs-lookup"><span data-stu-id="86c2d-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="86c2d-104">\[Die **updatebinary** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="86c2d-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86c2d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86c2d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86c2d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="86c2d-107">Die **updatebinary** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), mit dem die Bits, die in einer elementaren Datei vorhanden sind, mit den im APDU-Befehl angegebenen Bits aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="86c2d-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c2d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86c2d-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="86c2d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86c2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c2d-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c2d-111">Offset bis zum Schreib Speicherort (Update) in der Binärdatei ab dem Anfang der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="86c2d-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="86c2d-112">Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt. der Wert von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86c2d-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="86c2d-113">Wenn "B8 = 0" in P1 \| \| ist, ist P1 P2 der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86c2d-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="86c2d-114">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c2d-115">Offset bis zum Schreib Speicherort (Update) in der Binärdatei ab dem Anfang der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="86c2d-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="86c2d-116">Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt. der Wert von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86c2d-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="86c2d-117">Wenn "B8 = 0" in P1 \| \| ist, ist P1 P2 der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86c2d-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="86c2d-118">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c2d-119">Ein Zeiger auf die Zeichenfolge der zu aktualisierenden Dateneinheiten.</span><span class="sxs-lookup"><span data-stu-id="86c2d-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="86c2d-120">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c2d-121">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="86c2d-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="86c2d-122">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="86c2d-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="86c2d-123">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86c2d-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c2d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86c2d-124">Return value</span></span>

<span data-ttu-id="86c2d-125">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="86c2d-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="86c2d-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86c2d-126">Return code</span></span>                                                                                   | <span data-ttu-id="86c2d-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86c2d-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="86c2d-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86c2d-129">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="86c2d-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="86c2d-130"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="86c2d-131">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="86c2d-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="86c2d-132"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86c2d-133">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="86c2d-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="86c2d-134"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86c2d-135">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="86c2d-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="86c2d-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86c2d-136">Remarks</span></span>

<span data-ttu-id="86c2d-137">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der Smartcard den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="86c2d-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="86c2d-138">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="86c2d-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="86c2d-139">Elementare Dateien ohne transparente Struktur können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="86c2d-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="86c2d-140">Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="86c2d-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="86c2d-141">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="86c2d-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="86c2d-142">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="86c2d-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="86c2d-143">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="86c2d-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86c2d-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c2d-144">Requirements</span></span>



| <span data-ttu-id="86c2d-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86c2d-145">Requirement</span></span> | <span data-ttu-id="86c2d-146">Wert</span><span class="sxs-lookup"><span data-stu-id="86c2d-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86c2d-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86c2d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="86c2d-148">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="86c2d-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86c2d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="86c2d-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c2d-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86c2d-151">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="86c2d-151">End of client support</span></span><br/>    | <span data-ttu-id="86c2d-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="86c2d-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="86c2d-153">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="86c2d-153">End of server support</span></span><br/>    | <span data-ttu-id="86c2d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86c2d-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="86c2d-155">Header</span><span class="sxs-lookup"><span data-stu-id="86c2d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c2d-156"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86c2d-157">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="86c2d-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="86c2d-158"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86c2d-159">DLL</span><span class="sxs-lookup"><span data-stu-id="86c2d-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c2d-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c2d-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86c2d-161">IID</span><span class="sxs-lookup"><span data-stu-id="86c2d-161">IID</span></span><br/>                      | <span data-ttu-id="86c2d-162">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="86c2d-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="86c2d-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86c2d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c2d-164">**Erasebinary**</span><span class="sxs-lookup"><span data-stu-id="86c2d-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="86c2d-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="86c2d-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="86c2d-166">**"Read Binary"**</span><span class="sxs-lookup"><span data-stu-id="86c2d-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="86c2d-167">**"Write Binary"**</span><span class="sxs-lookup"><span data-stu-id="86c2d-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
