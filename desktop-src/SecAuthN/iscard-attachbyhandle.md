---
description: Fügt das iscard-Objekt an ein geöffnetes und konfiguriertes smartcardhandle an.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'Iscard:: attachbyhandle-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364183"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="7a1a0-103">Iscard:: attachbyhandle-Methode</span><span class="sxs-lookup"><span data-stu-id="7a1a0-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="7a1a0-104">\[Die **attachbyhandle** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7a1a0-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7a1a0-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7a1a0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7a1a0-107">Die **attachbyhandle** -Methode fügt das [**iscard**](iscard.md) -Objekt an ein geöffnetes und konfiguriertes [*smartcardhandle*](../secgloss/s-gly.md) an.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a1a0-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="7a1a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a1a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a1a0-110">*hCard* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a1a0-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a0-111">Ein Handle für eine geöffnete Verbindung zu einer Smartcard.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a1a0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a1a0-112">Return value</span></span>

<span data-ttu-id="7a1a0-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7a1a0-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7a1a0-114">Return code</span></span>                                                                                  | <span data-ttu-id="7a1a0-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a1a0-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7a1a0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a0-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7a1a0-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="7a1a0-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a0-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7a1a0-119">Der *hCard* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a1a0-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a1a0-120">Remarks</span></span>

<span data-ttu-id="7a1a0-121">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7a1a0-122">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7a1a0-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="7a1a0-123">Wenn Sie die Verwendung des Handles abgeschlossen haben, geben Sie die Anlage frei, indem Sie die [**iscard::D Etach**](iscard-detach.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7a1a0-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a1a0-124">Examples</span></span>

<span data-ttu-id="7a1a0-125">Im folgenden Beispiel wird das Anfügen an ein smartcardhandle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a1a0-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="7a1a0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a1a0-126">Requirements</span></span>



| <span data-ttu-id="7a1a0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a1a0-127">Requirement</span></span> | <span data-ttu-id="7a1a0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7a1a0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1a0-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a1a0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1a0-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a1a0-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7a1a0-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a1a0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1a0-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a1a0-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a1a0-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7a1a0-133">End of client support</span></span><br/>    | <span data-ttu-id="7a1a0-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a1a0-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7a1a0-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7a1a0-135">End of server support</span></span><br/>    | <span data-ttu-id="7a1a0-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a1a0-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7a1a0-137">Header</span><span class="sxs-lookup"><span data-stu-id="7a1a0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a1a0-138"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a0-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a1a0-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7a1a0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a1a0-140"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a0-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a1a0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7a1a0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a1a0-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a0-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a1a0-143">IID</span><span class="sxs-lookup"><span data-stu-id="7a1a0-143">IID</span></span><br/>                      | <span data-ttu-id="7a1a0-144">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="7a1a0-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7a1a0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a1a0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1a0-146">**Attachbyreader**</span><span class="sxs-lookup"><span data-stu-id="7a1a0-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="7a1a0-147">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="7a1a0-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="7a1a0-148">**\_cardhandle erhalten**</span><span class="sxs-lookup"><span data-stu-id="7a1a0-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="7a1a0-149">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="7a1a0-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="7a1a0-150">**Erneut**</span><span class="sxs-lookup"><span data-stu-id="7a1a0-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
