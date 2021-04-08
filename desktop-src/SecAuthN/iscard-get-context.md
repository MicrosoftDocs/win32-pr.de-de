---
description: Ruft das aktuelle Resource Manager-Kontext Handle ab. Diese Methode gibt ( \* pContext) = = NULL zurück, wenn kein Kontext festgelegt wurde.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Iscard:: get_Context-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867851"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="43fda-104">Iscard:: get- \_ Kontext Methode</span><span class="sxs-lookup"><span data-stu-id="43fda-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="43fda-105">\[Die **\_ Kontext** Methode "Get" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="43fda-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="43fda-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43fda-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43fda-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="43fda-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="43fda-108">Die **get \_ context** -Methode ruft das aktuelle [*Resource Manager-Kontext*](../secgloss/r-gly.md) Handle ab.</span><span class="sxs-lookup"><span data-stu-id="43fda-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="43fda-109">Diese Methode gibt ( \* *pContext*) = = **null** zurück, wenn kein Kontext festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="43fda-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="43fda-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="43fda-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="43fda-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="43fda-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fda-112">*pContext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43fda-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43fda-113">Zeiger auf den Kontext Handle bei Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="43fda-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fda-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43fda-114">Return value</span></span>

<span data-ttu-id="43fda-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="43fda-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="43fda-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="43fda-116">Return code</span></span>                                                                                  | <span data-ttu-id="43fda-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43fda-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="43fda-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43fda-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="43fda-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="43fda-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="43fda-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="43fda-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="43fda-121">Der *pContext* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="43fda-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="43fda-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="43fda-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="43fda-123">Ein fehlerhafter Zeiger wurde in *pContext* übergeben.</span><span class="sxs-lookup"><span data-stu-id="43fda-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43fda-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43fda-124">Remarks</span></span>

<span data-ttu-id="43fda-125">Der Resource Manager-Kontext wird festgelegt, indem die [*smartcardfunktion*](../secgloss/s-gly.md) " [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="43fda-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="43fda-126">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="43fda-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="43fda-127">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="43fda-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="43fda-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43fda-128">Examples</span></span>

<span data-ttu-id="43fda-129">Das folgende Beispiel zeigt, wie das aktuelle [*Resource Manager-Kontext*](../secgloss/r-gly.md) Handle abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="43fda-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="43fda-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43fda-130">Requirements</span></span>



| <span data-ttu-id="43fda-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43fda-131">Requirement</span></span> | <span data-ttu-id="43fda-132">Wert</span><span class="sxs-lookup"><span data-stu-id="43fda-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43fda-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43fda-133">Minimum supported client</span></span><br/> | <span data-ttu-id="43fda-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43fda-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="43fda-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43fda-135">Minimum supported server</span></span><br/> | <span data-ttu-id="43fda-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43fda-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43fda-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="43fda-137">End of client support</span></span><br/>    | <span data-ttu-id="43fda-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="43fda-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="43fda-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="43fda-139">End of server support</span></span><br/>    | <span data-ttu-id="43fda-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="43fda-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="43fda-141">Header</span><span class="sxs-lookup"><span data-stu-id="43fda-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="43fda-142"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="43fda-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="43fda-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="43fda-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="43fda-144"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43fda-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43fda-145">DLL</span><span class="sxs-lookup"><span data-stu-id="43fda-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43fda-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43fda-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="43fda-147">IID</span><span class="sxs-lookup"><span data-stu-id="43fda-147">IID</span></span><br/>                      | <span data-ttu-id="43fda-148">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="43fda-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="43fda-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43fda-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43fda-150">**\_ATR erhalten**</span><span class="sxs-lookup"><span data-stu-id="43fda-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="43fda-151">**\_cardhandle erhalten**</span><span class="sxs-lookup"><span data-stu-id="43fda-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="43fda-152">**get- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="43fda-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="43fda-153">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="43fda-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="43fda-154">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="43fda-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="43fda-155">**SCardEstablishContext**</span><span class="sxs-lookup"><span data-stu-id="43fda-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
