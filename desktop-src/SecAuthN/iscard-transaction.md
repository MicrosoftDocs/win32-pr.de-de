---
description: Führt einen Schreib-und Lesevorgang für den smartcardbefehl (Application Protocol Data Unit) aus.
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'Iscard:: Transaction-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356861"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="07e45-103">Iscard:: Transaction-Methode</span><span class="sxs-lookup"><span data-stu-id="07e45-103">ISCard::Transaction method</span></span>

<span data-ttu-id="07e45-104">\[Die **Transaktions** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="07e45-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="07e45-105">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="07e45-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="07e45-106">Die **Transaktions** Methode führt einen Schreib-und Lesevorgang für den [*smartcardbefehl*](../secgloss/s-gly.md) ([*Application Protocol Data Unit*](../secgloss/a-gly.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="07e45-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="07e45-107">Die Antwort Zeichenfolge von der Smartcard für die Befehls Zeichenfolge, die auf der Karte definiert ist, die an die Smartcard gesendet wurde, kann nach der Rückgabe dieser Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="07e45-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e45-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="07e45-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="07e45-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="07e45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e45-110">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07e45-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07e45-111">Ein Zeiger auf das Smartcard-Befehls Objekt.</span><span class="sxs-lookup"><span data-stu-id="07e45-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e45-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07e45-112">Return value</span></span>

<span data-ttu-id="07e45-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="07e45-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="07e45-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="07e45-114">Return code</span></span>                                                                                   | <span data-ttu-id="07e45-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07e45-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="07e45-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="07e45-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="07e45-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="07e45-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="07e45-119">Der *ppcmd* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="07e45-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="07e45-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="07e45-121">Ein fehlerhafter Zeiger wurde in *ppcmd* übergeben.</span><span class="sxs-lookup"><span data-stu-id="07e45-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="07e45-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="07e45-123">Der Arbeitsspeicher zum erfüllen der Anforderung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07e45-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07e45-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07e45-124">Remarks</span></span>

<span data-ttu-id="07e45-125">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="07e45-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="07e45-126">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="07e45-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="07e45-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07e45-127">Examples</span></span>

<span data-ttu-id="07e45-128">Das folgende Beispiel zeigt, wie Sie einen Schreib-und Lesevorgang für das Smartcard-Befehls Objekt ausführen.</span><span class="sxs-lookup"><span data-stu-id="07e45-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="07e45-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07e45-129">Requirements</span></span>



| <span data-ttu-id="07e45-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07e45-130">Requirement</span></span> | <span data-ttu-id="07e45-131">Wert</span><span class="sxs-lookup"><span data-stu-id="07e45-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07e45-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07e45-132">Minimum supported client</span></span><br/> | <span data-ttu-id="07e45-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07e45-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="07e45-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07e45-134">Minimum supported server</span></span><br/> | <span data-ttu-id="07e45-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07e45-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07e45-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="07e45-136">End of client support</span></span><br/>    | <span data-ttu-id="07e45-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="07e45-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="07e45-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="07e45-138">End of server support</span></span><br/>    | <span data-ttu-id="07e45-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07e45-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="07e45-140">Header</span><span class="sxs-lookup"><span data-stu-id="07e45-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="07e45-141"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="07e45-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="07e45-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="07e45-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="07e45-144">DLL</span><span class="sxs-lookup"><span data-stu-id="07e45-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07e45-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e45-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="07e45-146">IID</span><span class="sxs-lookup"><span data-stu-id="07e45-146">IID</span></span><br/>                      | <span data-ttu-id="07e45-147">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="07e45-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="07e45-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07e45-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e45-149">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="07e45-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="07e45-150">**Attachbyreader**</span><span class="sxs-lookup"><span data-stu-id="07e45-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="07e45-151">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="07e45-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="07e45-152">**\_ATR erhalten**</span><span class="sxs-lookup"><span data-stu-id="07e45-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="07e45-153">**\_cardhandle erhalten**</span><span class="sxs-lookup"><span data-stu-id="07e45-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="07e45-154">**\_Kontext erhalten**</span><span class="sxs-lookup"><span data-stu-id="07e45-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="07e45-155">**get- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="07e45-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="07e45-156">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="07e45-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="07e45-157">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="07e45-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="07e45-158">**Sperrkarte**</span><span class="sxs-lookup"><span data-stu-id="07e45-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="07e45-159">**Erneut**</span><span class="sxs-lookup"><span data-stu-id="07e45-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="07e45-160">**Unlockcard**</span><span class="sxs-lookup"><span data-stu-id="07e45-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
