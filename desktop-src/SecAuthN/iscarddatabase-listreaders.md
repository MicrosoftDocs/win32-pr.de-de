---
description: Die listreaders-Methode ruft die Namen der Smartcardleser ab, die in der Smartcard-Datenbank registriert sind.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'Iscarddatabase:: listreaders-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368089"
---
# <a name="iscarddatabaselistreaders-method"></a><span data-ttu-id="d0c0d-103">Iscarddatabase:: listreaders-Methode</span><span class="sxs-lookup"><span data-stu-id="d0c0d-103">ISCardDatabase::ListReaders method</span></span>

<span data-ttu-id="d0c0d-104">\[Die **listreaders** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-104">\[The **ListReaders** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0c0d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0c0d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d0c0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d0c0d-107">Die **listreaders** -Methode ruft die Namen der [*Smartcardleser*](../secgloss/r-gly.md) ab, die in der [*Smartcard-Datenbank*](../secgloss/s-gly.md)registriert sind.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-107">The **ListReaders** method retrieves the names of the smart card [*readers*](../secgloss/r-gly.md) registered in the [*smart card database*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c0d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0c0d-108">Syntax</span></span>


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a><span data-ttu-id="d0c0d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0c0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c0d-110">*LocaleID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0c0d-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c0d-111">Sprach Lokalisierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="d0c0d-112">*ppreaders* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d0c0d-112">*ppReaders* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c0d-113">Zeiger auf ein SafeArray von bstrinray, das die Namen der Smartcardleser enthält, wenn erfolgreich. **Null** , wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card readers if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c0d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0c0d-114">Return value</span></span>

<span data-ttu-id="d0c0d-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d0c0d-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d0c0d-116">Return code</span></span>                                                                                   | <span data-ttu-id="d0c0d-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0c0d-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d0c0d-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0c0d-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-119">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="d0c0d-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d0c0d-121">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-121">Invalid parameter.</span></span><br/>                       |
| <dl> <span data-ttu-id="d0c0d-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d0c0d-123">Ein fehlerhafter Zeiger wurde in " *ppreaders*" übergeben.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-123">A bad pointer was passed in *ppReaders*.</span></span><br/> |
| <dl> <span data-ttu-id="d0c0d-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0c0d-125">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-125">Out of memory.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="d0c0d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0c0d-126">Remarks</span></span>

<span data-ttu-id="d0c0d-127">Rufen Sie zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md) oder [*Lesergruppen*](../secgloss/r-gly.md) [**listcards**](iscarddatabase-listcards.md) bzw. [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*reader groups*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="d0c0d-128">Zum Abrufen des [*primären Dienstanbieters*](../secgloss/p-gly.md) oder der Schnittstellen einer bestimmten Karte [**getprovidercardid**](iscarddatabase-getprovidercardid.md) bzw. [**listcardinterfaces**](iscarddatabase-listcardinterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="d0c0d-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="d0c0d-129">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="d0c0d-130">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d0c0d-131">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0c0d-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0c0d-132">Examples</span></span>

<span data-ttu-id="d0c0d-133">Das folgende Beispiel zeigt, wie Sie die Namen der Smartcardleser abrufen, die in der Smartcard-Datenbank registriert sind.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-133">The following example shows retrieving the names of the smart card readers registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="d0c0d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0c0d-134">Requirements</span></span>



| <span data-ttu-id="d0c0d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0c0d-135">Requirement</span></span> | <span data-ttu-id="d0c0d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d0c0d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c0d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0c0d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c0d-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0c0d-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0c0d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0c0d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c0d-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0c0d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0c0d-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d0c0d-141">End of client support</span></span><br/>    | <span data-ttu-id="d0c0d-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0c0d-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d0c0d-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d0c0d-143">End of server support</span></span><br/>    | <span data-ttu-id="d0c0d-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0c0d-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d0c0d-145">Header</span><span class="sxs-lookup"><span data-stu-id="d0c0d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c0d-146"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0c0d-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d0c0d-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0c0d-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0c0d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d0c0d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0c0d-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0d-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0c0d-151">IID</span><span class="sxs-lookup"><span data-stu-id="d0c0d-151">IID</span></span><br/>                      | <span data-ttu-id="d0c0d-152">IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0c0d-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0c0d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c0d-154">**Getprovidercardid**</span><span class="sxs-lookup"><span data-stu-id="d0c0d-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="d0c0d-155">**Iscarddatabase**</span><span class="sxs-lookup"><span data-stu-id="d0c0d-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="d0c0d-156">**Listcardinterfaces**</span><span class="sxs-lookup"><span data-stu-id="d0c0d-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="d0c0d-157">**Listcards**</span><span class="sxs-lookup"><span data-stu-id="d0c0d-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="d0c0d-158">**Listreadergroups**</span><span class="sxs-lookup"><span data-stu-id="d0c0d-158">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
