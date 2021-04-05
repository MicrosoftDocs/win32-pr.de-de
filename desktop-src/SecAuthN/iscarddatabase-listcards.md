---
description: Die listcards-Methode ruft alle smartcardnamen ab, die den angegebenen Schnittstellen Bezeichnerzeichen (GUIDs), der angegebenen ATR-Zeichenfolge oder beiden entsprechen.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Iscarddatabase:: List Cards-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751681"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="6f29b-103">Iscarddatabase:: listcards-Methode</span><span class="sxs-lookup"><span data-stu-id="6f29b-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="6f29b-104">\[Die **listcards** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6f29b-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6f29b-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f29b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6f29b-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6f29b-107">Die **listcards** -Methode ruft alle smartcardnamen ab, die den angegebenen Schnittstellen Bezeichnerzeichen (GUIDs), der angegebenen [*ATR-Zeichenfolge*](../secgloss/a-gly.md)oder beiden entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6f29b-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f29b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f29b-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="6f29b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f29b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f29b-110">*Patr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f29b-111">Zeiger auf eine [*Smartcard*](../secgloss/s-gly.md) -ATR-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6f29b-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="6f29b-112">Die ATR-Zeichenfolge muss in einen [**ibytebuffer**](ibytebuffer.md)gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="6f29b-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f29b-113">*pinterfaceguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f29b-114">Zeiger auf ein SafeArray von COM-Schnittstellen Bezeichners (GUIDs) im BSTR-Format.</span><span class="sxs-lookup"><span data-stu-id="6f29b-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="6f29b-115">*LocaleID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f29b-116">Der Bezeichner der Sprachlokalisierung.</span><span class="sxs-lookup"><span data-stu-id="6f29b-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6f29b-117">*ppcardnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f29b-118">Zeiger auf ein SafeArray von bstrinray, das die Namen der Smartcards enthält, die die Suchparameter bei erfolgreicher Ausführung erfüllt haben. **Null** , wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6f29b-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f29b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f29b-119">Return value</span></span>

<span data-ttu-id="6f29b-120">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6f29b-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6f29b-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6f29b-121">Return code</span></span>                                                                                   | <span data-ttu-id="6f29b-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f29b-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6f29b-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6f29b-124">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6f29b-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6f29b-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6f29b-126">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f29b-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6f29b-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6f29b-128">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6f29b-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6f29b-129"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6f29b-130">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6f29b-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6f29b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f29b-131">Remarks</span></span>

<span data-ttu-id="6f29b-132">Um [*alle bekannten Reader*](../secgloss/r-gly.md) oder [*Reader*](../secgloss/r-gly.md)abzurufen, rufen Sie [**listreaders**](iscarddatabase-listreaders.md) bzw. [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.</span><span class="sxs-lookup"><span data-stu-id="6f29b-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="6f29b-133">Zum Abrufen des [*primären Dienstanbieter*](../secgloss/p-gly.md) oder der Schnittstellen einer bestimmten Karte [**getprovidercardid**](iscarddatabase-getprovidercardid.md) bzw. [**listcardinterfaces**](iscarddatabase-listcardinterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="6f29b-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="6f29b-134">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="6f29b-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="6f29b-135">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6f29b-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6f29b-136">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6f29b-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6f29b-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f29b-137">Examples</span></span>

<span data-ttu-id="6f29b-138">Im folgenden Beispiel wird gezeigt, wie die smartcardnamen abgerufen werden, die der angegebenen ATR-Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6f29b-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6f29b-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f29b-139">Requirements</span></span>



| <span data-ttu-id="6f29b-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f29b-140">Requirement</span></span> | <span data-ttu-id="6f29b-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6f29b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f29b-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f29b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6f29b-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6f29b-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f29b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6f29b-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f29b-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f29b-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6f29b-146">End of client support</span></span><br/>    | <span data-ttu-id="6f29b-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f29b-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6f29b-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6f29b-148">End of server support</span></span><br/>    | <span data-ttu-id="6f29b-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f29b-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6f29b-150">Header</span><span class="sxs-lookup"><span data-stu-id="6f29b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f29b-151"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f29b-152">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6f29b-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f29b-153"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f29b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="6f29b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f29b-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f29b-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f29b-156">IID</span><span class="sxs-lookup"><span data-stu-id="6f29b-156">IID</span></span><br/>                      | <span data-ttu-id="6f29b-157">IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="6f29b-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6f29b-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f29b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f29b-159">**Getprovidercardid**</span><span class="sxs-lookup"><span data-stu-id="6f29b-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="6f29b-160">**Iscarddatabase**</span><span class="sxs-lookup"><span data-stu-id="6f29b-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="6f29b-161">**Listcardinterfaces**</span><span class="sxs-lookup"><span data-stu-id="6f29b-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="6f29b-162">**Listreadergroups**</span><span class="sxs-lookup"><span data-stu-id="6f29b-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="6f29b-163">**Listreaders**</span><span class="sxs-lookup"><span data-stu-id="6f29b-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
