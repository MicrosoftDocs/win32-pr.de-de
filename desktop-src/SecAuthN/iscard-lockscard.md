---
description: Die lockscard-Methode beansprucht exklusiven Zugriff auf die Smartcard.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'Iscard:: lockscard-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217763"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="67c0d-103">Iscard:: lockscard-Methode</span><span class="sxs-lookup"><span data-stu-id="67c0d-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="67c0d-104">\[Die **lockscard** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="67c0d-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="67c0d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67c0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="67c0d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="67c0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="67c0d-107">Die **lockscard** -Methode beansprucht exklusiven Zugriff auf die [*Smartcard*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="67c0d-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="67c0d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67c0d-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="67c0d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="67c0d-109">Parameters</span></span>

<span data-ttu-id="67c0d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="67c0d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67c0d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67c0d-111">Return value</span></span>

<span data-ttu-id="67c0d-112">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="67c0d-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="67c0d-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="67c0d-113">Return code</span></span>                                                                          | <span data-ttu-id="67c0d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67c0d-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="67c0d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="67c0d-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="67c0d-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="67c0d-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67c0d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67c0d-117">Remarks</span></span>

<span data-ttu-id="67c0d-118">Zusätzlich zum oben aufgeführten com-Fehlercode gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="67c0d-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="67c0d-119">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="67c0d-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="67c0d-120">Um die Smartcard zu entsperren, wenden Sie die [**iscard:: unlockscard**](iscard-unlockscard.md) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="67c0d-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="67c0d-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67c0d-121">Examples</span></span>

<span data-ttu-id="67c0d-122">Das folgende Beispiel zeigt, wie Sie exklusiven Zugriff auf die Smartcard erwerben.</span><span class="sxs-lookup"><span data-stu-id="67c0d-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="67c0d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67c0d-123">Requirements</span></span>



| <span data-ttu-id="67c0d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67c0d-124">Requirement</span></span> | <span data-ttu-id="67c0d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="67c0d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67c0d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67c0d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="67c0d-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67c0d-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="67c0d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67c0d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="67c0d-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67c0d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67c0d-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="67c0d-130">End of client support</span></span><br/>    | <span data-ttu-id="67c0d-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67c0d-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="67c0d-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="67c0d-132">End of server support</span></span><br/>    | <span data-ttu-id="67c0d-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67c0d-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="67c0d-134">Header</span><span class="sxs-lookup"><span data-stu-id="67c0d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c0d-135"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="67c0d-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="67c0d-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="67c0d-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="67c0d-137"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67c0d-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67c0d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="67c0d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67c0d-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67c0d-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="67c0d-140">IID</span><span class="sxs-lookup"><span data-stu-id="67c0d-140">IID</span></span><br/>                      | <span data-ttu-id="67c0d-141">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="67c0d-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="67c0d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67c0d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c0d-143">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="67c0d-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="67c0d-144">**Unlockcard**</span><span class="sxs-lookup"><span data-stu-id="67c0d-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
