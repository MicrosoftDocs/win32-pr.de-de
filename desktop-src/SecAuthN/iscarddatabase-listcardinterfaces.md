---
description: Die listcardinterfaces-Methode ruft die Bezeichner (GUIDs) aller Schnittstellen ab, die für die angegebene Smartcard unterstützt werden.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Iscarddatabase:: listcardinterfaces-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214406"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a><span data-ttu-id="5a1fb-103">Iscarddatabase:: listcardinterfaces-Methode</span><span class="sxs-lookup"><span data-stu-id="5a1fb-103">ISCardDatabase::ListCardInterfaces method</span></span>

<span data-ttu-id="5a1fb-104">\[Die **listcardinterfaces** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-104">\[The **ListCardInterfaces** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5a1fb-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a1fb-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5a1fb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5a1fb-107">Die **listcardinterfaces** -Methode ruft die Bezeichner (GUIDs) aller Schnittstellen ab, die für die angegebene [*Smartcard*](../secgloss/s-gly.md)unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-107">The **ListCardInterfaces** method retrieves the identifiers (GUIDs) of all the interfaces supported for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1fb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a1fb-108">Syntax</span></span>


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a><span data-ttu-id="5a1fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a1fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a1fb-110">*bstrincardname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a1fb-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1fb-111">Der Name der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="5a1fb-112">*ppinterfaceguids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a1fb-112">*ppInterfaceGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1fb-113">Zeiger auf die Schnittstellen-GUIDs, wenn erfolgreich; **Null** , wenn der Vorgang fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="5a1fb-113">Pointer to the interface GUIDs if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a1fb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a1fb-114">Return value</span></span>

<span data-ttu-id="5a1fb-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5a1fb-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5a1fb-116">Return code</span></span>                                                                                   | <span data-ttu-id="5a1fb-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a1fb-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="5a1fb-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a1fb-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="5a1fb-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5a1fb-121">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="5a1fb-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5a1fb-123">Ein fehlerhafter Zeiger wurde in *ppinterfaceguids* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-123">A bad pointer was passed in *ppInterfaceGuids*.</span></span><br/> |
| <dl> <span data-ttu-id="5a1fb-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5a1fb-125">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="5a1fb-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a1fb-126">Remarks</span></span>

<span data-ttu-id="5a1fb-127">Rufen Sie [**getprovidercardid**](iscarddatabase-getprovidercardid.md)auf, um den [*primären Dienstanbieter*](../secgloss/p-gly.md) der Smartcard abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-127">To retrieve the [*primary service provider*](../secgloss/p-gly.md) of the smart card, call [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span></span>

<span data-ttu-id="5a1fb-128">Rufen Sie zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md), [*Leser*](../secgloss/r-gly.md)und [*Lesergruppen*](../secgloss/r-gly.md) [**listcards**](iscarddatabase-listcards.md), [**listreaders**](iscarddatabase-listreaders.md)und [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md), and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="5a1fb-129">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="5a1fb-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="5a1fb-130">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5a1fb-131">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5a1fb-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a1fb-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a1fb-132">Examples</span></span>

<span data-ttu-id="5a1fb-133">Das folgende Beispiel zeigt das Abrufen der Bezeichner der Schnittstellen, die für die angegebene Smartcard unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-133">The following example shows retrieving the identifiers of the interfaces supported for the specified smart card.</span></span>


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a><span data-ttu-id="5a1fb-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a1fb-134">Requirements</span></span>



| <span data-ttu-id="5a1fb-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a1fb-135">Requirement</span></span> | <span data-ttu-id="5a1fb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="5a1fb-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1fb-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a1fb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1fb-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a1fb-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5a1fb-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a1fb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1fb-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a1fb-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a1fb-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5a1fb-141">End of client support</span></span><br/>    | <span data-ttu-id="5a1fb-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a1fb-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5a1fb-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5a1fb-143">End of server support</span></span><br/>    | <span data-ttu-id="5a1fb-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a1fb-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5a1fb-145">Header</span><span class="sxs-lookup"><span data-stu-id="5a1fb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1fb-146"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a1fb-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5a1fb-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a1fb-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a1fb-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5a1fb-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a1fb-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a1fb-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a1fb-151">IID</span><span class="sxs-lookup"><span data-stu-id="5a1fb-151">IID</span></span><br/>                      | <span data-ttu-id="5a1fb-152">IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5a1fb-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a1fb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1fb-154">**Getprovidercardid**</span><span class="sxs-lookup"><span data-stu-id="5a1fb-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="5a1fb-155">**Iscarddatabase**</span><span class="sxs-lookup"><span data-stu-id="5a1fb-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="5a1fb-156">**Listcards**</span><span class="sxs-lookup"><span data-stu-id="5a1fb-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="5a1fb-157">**Listreadergroups**</span><span class="sxs-lookup"><span data-stu-id="5a1fb-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="5a1fb-158">**Listreaders**</span><span class="sxs-lookup"><span data-stu-id="5a1fb-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
