---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der einen Teil des Inhalts einer elementaren Datei sequenziell auf den logischen Lösch Zustand festlegt, beginnend bei einem bestimmten Offset.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816:: erasebinary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373303"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="aae8b-103">ISCardISO7816:: erasebinary-Methode</span><span class="sxs-lookup"><span data-stu-id="aae8b-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="aae8b-104">\[Die **erasebinary** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="aae8b-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aae8b-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aae8b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aae8b-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="aae8b-107">Die **erasebinary** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der einen Teil des Inhalts einer elementaren Datei sequenziell auf den logischen Lösch Zustand festlegt, beginnend bei einem bestimmten Offset.</span><span class="sxs-lookup"><span data-stu-id="aae8b-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae8b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aae8b-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="aae8b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aae8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae8b-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae8b-111">RFU-Position.</span><span class="sxs-lookup"><span data-stu-id="aae8b-111">RFU position.</span></span>

<span data-ttu-id="aae8b-112">Wenn "B8 = 1" in P1 ist, werden B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, der Wert für "B5 bis B1" von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, der vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).</span><span class="sxs-lookup"><span data-stu-id="aae8b-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="aae8b-113">Wenn in P1 den Wert 0 (null) hat, \| \| ist P1 P2 der Offset des ersten Bytes, das vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).</span><span class="sxs-lookup"><span data-stu-id="aae8b-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="aae8b-114">Wenn das Datenfeld vorhanden ist, wird der Offset der ersten Dateneinheit, die nicht gelöscht werden soll, codiert.</span><span class="sxs-lookup"><span data-stu-id="aae8b-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="aae8b-115">Dieser Offset muss höher sein als der in P1-P2 codierte.</span><span class="sxs-lookup"><span data-stu-id="aae8b-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="aae8b-116">Wenn das Datenfeld leer ist, wird der Befehl bis zum Ende der Datei gelöscht.</span><span class="sxs-lookup"><span data-stu-id="aae8b-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="aae8b-117">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae8b-118">RFU-Position.</span><span class="sxs-lookup"><span data-stu-id="aae8b-118">RFU position.</span></span>

<span data-ttu-id="aae8b-119">Wenn "B8 = 1" in P1 ist, werden B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, der Wert für "B5 bis B1" von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, der vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).</span><span class="sxs-lookup"><span data-stu-id="aae8b-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="aae8b-120">Wenn in P1 den Wert 0 (null) hat, \| \| ist P1 P2 der Offset des ersten Bytes, das vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).</span><span class="sxs-lookup"><span data-stu-id="aae8b-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="aae8b-121">Wenn das Datenfeld vorhanden ist, wird der Offset der ersten Dateneinheit, die nicht gelöscht werden soll, codiert.</span><span class="sxs-lookup"><span data-stu-id="aae8b-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="aae8b-122">Dieser Offset muss höher sein als der in P1-P2 codierte.</span><span class="sxs-lookup"><span data-stu-id="aae8b-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="aae8b-123">Wenn das Datenfeld leer ist, wird der Befehl bis zum Ende der Datei gelöscht.</span><span class="sxs-lookup"><span data-stu-id="aae8b-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="aae8b-124">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae8b-125">Ein Zeiger auf die Daten, die den Löschbereich angeben.</span><span class="sxs-lookup"><span data-stu-id="aae8b-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="aae8b-126">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="aae8b-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aae8b-127">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae8b-128">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="aae8b-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="aae8b-129">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="aae8b-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="aae8b-130">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mithilfe des *ppcmd* -Zeigers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aae8b-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae8b-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aae8b-131">Return value</span></span>

<span data-ttu-id="aae8b-132">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="aae8b-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="aae8b-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="aae8b-133">Return code</span></span>                                                                                   | <span data-ttu-id="aae8b-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aae8b-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="aae8b-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aae8b-136">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aae8b-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="aae8b-137"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aae8b-138">Ein ungültiger Parameter wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="aae8b-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="aae8b-139"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aae8b-140">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aae8b-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="aae8b-141"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aae8b-142">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="aae8b-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="aae8b-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aae8b-143">Remarks</span></span>

<span data-ttu-id="aae8b-144">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="aae8b-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="aae8b-145">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aae8b-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="aae8b-146">Elementare Dateien ohne transparente Struktur können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="aae8b-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="aae8b-147">Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="aae8b-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="aae8b-148">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="aae8b-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="aae8b-149">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="aae8b-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="aae8b-150">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="aae8b-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aae8b-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aae8b-151">Requirements</span></span>



| <span data-ttu-id="aae8b-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aae8b-152">Requirement</span></span> | <span data-ttu-id="aae8b-153">Wert</span><span class="sxs-lookup"><span data-stu-id="aae8b-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aae8b-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aae8b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="aae8b-155">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aae8b-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aae8b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="aae8b-157">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aae8b-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aae8b-158">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="aae8b-158">End of client support</span></span><br/>    | <span data-ttu-id="aae8b-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aae8b-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="aae8b-160">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="aae8b-160">End of server support</span></span><br/>    | <span data-ttu-id="aae8b-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aae8b-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="aae8b-162">Header</span><span class="sxs-lookup"><span data-stu-id="aae8b-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae8b-163"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aae8b-164">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="aae8b-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="aae8b-165"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aae8b-166">DLL</span><span class="sxs-lookup"><span data-stu-id="aae8b-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aae8b-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aae8b-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aae8b-168">IID</span><span class="sxs-lookup"><span data-stu-id="aae8b-168">IID</span></span><br/>                      | <span data-ttu-id="aae8b-169">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="aae8b-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="aae8b-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aae8b-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae8b-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="aae8b-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="aae8b-172">**"Read Binary"**</span><span class="sxs-lookup"><span data-stu-id="aae8b-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="aae8b-173">**Updatebinary**</span><span class="sxs-lookup"><span data-stu-id="aae8b-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="aae8b-174">**"Write Binary"**</span><span class="sxs-lookup"><span data-stu-id="aae8b-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
