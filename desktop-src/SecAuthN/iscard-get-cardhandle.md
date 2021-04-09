---
description: Ruft das Handle für eine verbundene Smartcard ab. Diese Methode gibt ( \* phandle) = = NULL zurück, wenn keine Verbindung besteht.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'Iscard:: get_CardHandle-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958703"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="e21b5-104">Iscard:: get \_ cardhandle-Methode</span><span class="sxs-lookup"><span data-stu-id="e21b5-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="e21b5-105">\[Die **get \_ cardhandle** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e21b5-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e21b5-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e21b5-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e21b5-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e21b5-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e21b5-108">Die **get \_ cardhandle** -Methode ruft das Handle für eine verbundene [*Smartcard*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="e21b5-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="e21b5-109">Diese Methode gibt ( \* phandle) = = **null** zurück, wenn keine Verbindung besteht.</span><span class="sxs-lookup"><span data-stu-id="e21b5-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="e21b5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e21b5-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="e21b5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e21b5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e21b5-112">*phandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e21b5-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e21b5-113">Zeiger auf den Karten Handle bei Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="e21b5-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e21b5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e21b5-114">Return value</span></span>

<span data-ttu-id="e21b5-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e21b5-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e21b5-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e21b5-116">Return code</span></span>                                                                                  | <span data-ttu-id="e21b5-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e21b5-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="e21b5-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e21b5-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e21b5-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e21b5-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="e21b5-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e21b5-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e21b5-121">Der *phandle* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e21b5-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="e21b5-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e21b5-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e21b5-123">Ein ungültiger Zeiger wurde in *phandle* übergeben.</span><span class="sxs-lookup"><span data-stu-id="e21b5-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e21b5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e21b5-124">Remarks</span></span>

<span data-ttu-id="e21b5-125">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e21b5-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e21b5-126">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e21b5-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e21b5-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e21b5-127">Examples</span></span>

<span data-ttu-id="e21b5-128">Das folgende Beispiel zeigt das Abrufen des Smartcard-Handles.</span><span class="sxs-lookup"><span data-stu-id="e21b5-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="e21b5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e21b5-129">Requirements</span></span>



| <span data-ttu-id="e21b5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e21b5-130">Requirement</span></span> | <span data-ttu-id="e21b5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e21b5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e21b5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e21b5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e21b5-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e21b5-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e21b5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e21b5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e21b5-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e21b5-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e21b5-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e21b5-136">End of client support</span></span><br/>    | <span data-ttu-id="e21b5-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e21b5-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e21b5-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e21b5-138">End of server support</span></span><br/>    | <span data-ttu-id="e21b5-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e21b5-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e21b5-140">Header</span><span class="sxs-lookup"><span data-stu-id="e21b5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e21b5-141"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e21b5-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="e21b5-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e21b5-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="e21b5-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e21b5-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e21b5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e21b5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e21b5-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e21b5-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e21b5-146">IID</span><span class="sxs-lookup"><span data-stu-id="e21b5-146">IID</span></span><br/>                      | <span data-ttu-id="e21b5-147">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="e21b5-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e21b5-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e21b5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e21b5-149">**\_ATR erhalten**</span><span class="sxs-lookup"><span data-stu-id="e21b5-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="e21b5-150">**\_Kontext erhalten**</span><span class="sxs-lookup"><span data-stu-id="e21b5-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="e21b5-151">**get- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="e21b5-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="e21b5-152">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="e21b5-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="e21b5-153">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="e21b5-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
