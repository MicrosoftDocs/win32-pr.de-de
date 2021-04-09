---
description: Gibt exklusiven Zugriff auf die Smartcard frei.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: 'Iscard:: unlockscard-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68907e157e60518d1df3855fbca69709f2c21437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754185"
---
# <a name="iscardunlockscard-method"></a><span data-ttu-id="f0ee4-103">Iscard:: unlockscard-Methode</span><span class="sxs-lookup"><span data-stu-id="f0ee4-103">ISCard::UnlockSCard method</span></span>

<span data-ttu-id="f0ee4-104">\[Die **unlockscard** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-104">\[The **UnlockScard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f0ee4-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f0ee4-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="f0ee4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f0ee4-107">Die **unlockscard** -Methode gibt exklusiven Zugriff auf die [*Smartcard*](../secgloss/s-gly.md)frei.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-107">The **UnlockScard** method releases exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ee4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0ee4-108">Syntax</span></span>


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="f0ee4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0ee4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ee4-110">*Disposition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0ee4-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ee4-111">Gibt an, was mit der Karte im verbundenen [*Reader*](../secgloss/r-gly.md)geschehen soll.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="f0ee4-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f0ee4-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="f0ee4-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0ee4-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="f0ee4-114"><dt>**Lassen Sie**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="f0ee4-115">Verlässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f0ee4-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="f0ee4-116"><dt>**Festlegen**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="f0ee4-117">Setzt die Smartcard auf einen bekannten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="f0ee4-118"><dt>**Nicht mehr**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="f0ee4-119">Entfernt die Stromversorgung von der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="f0ee4-120"><dt>**Auswerfen**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="f0ee4-121">Fügt die Smartcard ein, wenn der Reader über Auswerfen-Funktionen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ee4-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0ee4-122">Return value</span></span>

<span data-ttu-id="f0ee4-123">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f0ee4-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f0ee4-124">Return code</span></span>                                                                                  | <span data-ttu-id="f0ee4-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0ee4-125">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="f0ee4-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f0ee4-127">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-127">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="f0ee4-128"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f0ee4-129">Der *Disposition* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-129">The *Disposition* parameter is not valid</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0ee4-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0ee4-130">Remarks</span></span>

<span data-ttu-id="f0ee4-131">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f0ee4-132">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f0ee4-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f0ee4-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0ee4-133">Examples</span></span>

<span data-ttu-id="f0ee4-134">Das folgende Beispiel zeigt, wie Sie exklusiven Zugriff auf die Smartcard freigeben.</span><span class="sxs-lookup"><span data-stu-id="f0ee4-134">The following example shows releasing exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f0ee4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0ee4-135">Requirements</span></span>



| <span data-ttu-id="f0ee4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0ee4-136">Requirement</span></span> | <span data-ttu-id="f0ee4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f0ee4-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ee4-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0ee4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ee4-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0ee4-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0ee4-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0ee4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ee4-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0ee4-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0ee4-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f0ee4-142">End of client support</span></span><br/>    | <span data-ttu-id="f0ee4-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0ee4-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f0ee4-144">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f0ee4-144">End of server support</span></span><br/>    | <span data-ttu-id="f0ee4-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0ee4-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f0ee4-146">Header</span><span class="sxs-lookup"><span data-stu-id="f0ee4-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ee4-147"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0ee4-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f0ee4-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0ee4-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0ee4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ee4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0ee4-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee4-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0ee4-152">IID</span><span class="sxs-lookup"><span data-stu-id="f0ee4-152">IID</span></span><br/>                      | <span data-ttu-id="f0ee4-153">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="f0ee4-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f0ee4-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0ee4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ee4-155">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="f0ee4-155">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="f0ee4-156">**Sperrkarte**</span><span class="sxs-lookup"><span data-stu-id="f0ee4-156">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> </dl>

 

 
