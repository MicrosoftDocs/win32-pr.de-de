---
description: Die getprovidercardid-Methode ruft den Bezeichner (GUID) des primären Dienstanbieters für die angegebene Smartcard ab.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Iscarddatabase:: getprovidercardid-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758826"
---
# <a name="iscarddatabasegetprovidercardid-method"></a><span data-ttu-id="b9e5c-103">Iscarddatabase:: getprovidercardid-Methode</span><span class="sxs-lookup"><span data-stu-id="b9e5c-103">ISCardDatabase::GetProviderCardId method</span></span>

<span data-ttu-id="b9e5c-104">\[Die **getprovidercardid** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-104">\[The **GetProviderCardId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9e5c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b9e5c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b9e5c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b9e5c-107">Die **getprovidercardid** -Methode ruft den Bezeichner (GUID) des [*primären Dienstanbieters*](../secgloss/p-gly.md) für die angegebene [*Smartcard*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-107">The **GetProviderCardId** method retrieves the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e5c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9e5c-108">Syntax</span></span>


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a><span data-ttu-id="b9e5c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9e5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e5c-110">*bstrincardname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9e5c-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e5c-111">Der Name der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="b9e5c-112">*ppguidproviderid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9e5c-112">*ppguidProviderId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e5c-113">Zeiger auf den Bezeichner des primären Dienstanbieters (GUID), wenn erfolgreich; **Null** , wenn der Vorgang fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="b9e5c-113">Pointer to the primary service provider's identifier (GUID) if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e5c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9e5c-114">Return value</span></span>

<span data-ttu-id="b9e5c-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b9e5c-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b9e5c-116">Return code</span></span>                                                                                   | <span data-ttu-id="b9e5c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9e5c-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="b9e5c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b9e5c-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="b9e5c-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b9e5c-121">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="b9e5c-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b9e5c-123">Ein fehlerhafter Zeiger wurde in *ppguidproviderid* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-123">A bad pointer was passed in *ppguidProviderId*.</span></span><br/> |
| <dl> <span data-ttu-id="b9e5c-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b9e5c-125">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="b9e5c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9e5c-126">Remarks</span></span>

<span data-ttu-id="b9e5c-127">Um die Schnittstellen der Smartcard aufzulisten, müssen Sie [**listcardinterfaces**](iscarddatabase-listcardinterfaces.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-127">To list the interfaces of the smart card, call [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span></span>

<span data-ttu-id="b9e5c-128">Rufen Sie zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md), [*Leser*](../secgloss/r-gly.md) und [*Lesergruppen*](../secgloss/r-gly.md) [**listcards**](iscarddatabase-listcards.md), [**listreaders**](iscarddatabase-listreaders.md)und [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md) and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="b9e5c-129">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5c-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="b9e5c-130">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b9e5c-131">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5c-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9e5c-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9e5c-132">Examples</span></span>

<span data-ttu-id="b9e5c-133">Das folgende Beispiel zeigt, wie der Bezeichner des primären Dienstanbieters für die angegebene Smartcard abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-133">The following example shows retrieving the identifier of the primary service provider for the specified smart card.</span></span>


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="b9e5c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9e5c-134">Requirements</span></span>



| <span data-ttu-id="b9e5c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9e5c-135">Requirement</span></span> | <span data-ttu-id="b9e5c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b9e5c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e5c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9e5c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e5c-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9e5c-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b9e5c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9e5c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e5c-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9e5c-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9e5c-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b9e5c-141">End of client support</span></span><br/>    | <span data-ttu-id="b9e5c-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9e5c-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b9e5c-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b9e5c-143">End of server support</span></span><br/>    | <span data-ttu-id="b9e5c-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9e5c-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b9e5c-145">Header</span><span class="sxs-lookup"><span data-stu-id="b9e5c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e5c-146"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9e5c-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b9e5c-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9e5c-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b9e5c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b9e5c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9e5c-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9e5c-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9e5c-151">IID</span><span class="sxs-lookup"><span data-stu-id="b9e5c-151">IID</span></span><br/>                      | <span data-ttu-id="b9e5c-152">IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="b9e5c-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b9e5c-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9e5c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e5c-154">**Iscarddatabase**</span><span class="sxs-lookup"><span data-stu-id="b9e5c-154">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="b9e5c-155">**Listcardinterfaces**</span><span class="sxs-lookup"><span data-stu-id="b9e5c-155">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="b9e5c-156">**Listcards**</span><span class="sxs-lookup"><span data-stu-id="b9e5c-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="b9e5c-157">**Listreadergroups**</span><span class="sxs-lookup"><span data-stu-id="b9e5c-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="b9e5c-158">**Listreaders**</span><span class="sxs-lookup"><span data-stu-id="b9e5c-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
