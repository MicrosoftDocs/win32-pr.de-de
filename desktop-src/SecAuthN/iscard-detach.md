---
description: Schließt die geöffnete Verbindung mit der Smartcard.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: Iscard::D Etach-Methode (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355346"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="dedd3-103">Iscard::D Etach-Methode</span><span class="sxs-lookup"><span data-stu-id="dedd3-103">ISCard::Detach method</span></span>

<span data-ttu-id="dedd3-104">\[Die **Detach** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dedd3-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dedd3-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dedd3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dedd3-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dedd3-107">Die **Detach** -Methode schließt die geöffnete Verbindung mit der [*Smartcard*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dedd3-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dedd3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dedd3-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="dedd3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dedd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dedd3-110">*Disposition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dedd3-111">Gibt an, was mit der Karte im verbundenen [*Reader*](../secgloss/r-gly.md)geschehen soll.</span><span class="sxs-lookup"><span data-stu-id="dedd3-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="dedd3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="dedd3-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="dedd3-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dedd3-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="dedd3-114"><dt>**Lassen Sie**</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="dedd3-115">Verlässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dedd3-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="dedd3-116"><dt>**Festlegen**</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="dedd3-117">Setzt die Smartcard auf einen bekannten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="dedd3-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="dedd3-118"><dt>**Nicht mehr**</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="dedd3-119">Entfernt die Stromversorgung von der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="dedd3-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="dedd3-120"><dt>**Auswerfen**</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="dedd3-121">Fügt die Smartcard ein, wenn der Reader über Auswerfen-Funktionen verfügt.</span><span class="sxs-lookup"><span data-stu-id="dedd3-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dedd3-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dedd3-122">Return value</span></span>

<span data-ttu-id="dedd3-123">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="dedd3-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dedd3-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dedd3-124">Return code</span></span>                                                                                  | <span data-ttu-id="dedd3-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dedd3-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dedd3-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dedd3-127">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="dedd3-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="dedd3-128"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dedd3-129">*Disposition* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dedd3-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="dedd3-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dedd3-130">Remarks</span></span>

<span data-ttu-id="dedd3-131">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="dedd3-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dedd3-132">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dedd3-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dedd3-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dedd3-133">Examples</span></span>

<span data-ttu-id="dedd3-134">Das folgende Beispiel zeigt das Schließen der Verbindung mit der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="dedd3-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="dedd3-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dedd3-135">Requirements</span></span>



| <span data-ttu-id="dedd3-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dedd3-136">Requirement</span></span> | <span data-ttu-id="dedd3-137">Wert</span><span class="sxs-lookup"><span data-stu-id="dedd3-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dedd3-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dedd3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dedd3-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dedd3-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dedd3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dedd3-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dedd3-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="dedd3-142">End of client support</span></span><br/>    | <span data-ttu-id="dedd3-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dedd3-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dedd3-144">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="dedd3-144">End of server support</span></span><br/>    | <span data-ttu-id="dedd3-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dedd3-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dedd3-146">Header</span><span class="sxs-lookup"><span data-stu-id="dedd3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedd3-147"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="dedd3-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dedd3-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="dedd3-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dedd3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="dedd3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dedd3-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dedd3-152">IID</span><span class="sxs-lookup"><span data-stu-id="dedd3-152">IID</span></span><br/>                      | <span data-ttu-id="dedd3-153">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="dedd3-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dedd3-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dedd3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedd3-155">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="dedd3-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="dedd3-156">**Attachbyreader**</span><span class="sxs-lookup"><span data-stu-id="dedd3-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="dedd3-157">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="dedd3-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="dedd3-158">**Erneut**</span><span class="sxs-lookup"><span data-stu-id="dedd3-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
