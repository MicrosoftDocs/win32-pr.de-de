---
description: Bestimmt die Länge (in Byte) der Anwendungsprotokoll Daten-Einheit (APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'Iscardcmd:: get_ApduReplyLength-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b62e67154ab48f8378c96a78c8bd54765962c3fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218511"
---
# <a name="iscardcmdget_apdureplylength-method"></a><span data-ttu-id="d13d6-103">Iscardcmd:: get \_ apdureumplylength-Methode</span><span class="sxs-lookup"><span data-stu-id="d13d6-103">ISCardCmd::get\_ApduReplyLength method</span></span>

<span data-ttu-id="d13d6-104">\[Die **get \_ apdureplylength** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d13d6-104">\[The **get\_ApduReplyLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d13d6-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d13d6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d13d6-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d13d6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d13d6-107">Die **get \_ apdureplylength** -Methode bestimmt die Länge (in Byte) der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="d13d6-107">The **get\_ApduReplyLength** method determines the length (in bytes) of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="d13d6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d13d6-108">Syntax</span></span>


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="d13d6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d13d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d13d6-110">*plsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d13d6-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d13d6-111">Zeiger auf die Größe der APDU-Antwortnachricht.</span><span class="sxs-lookup"><span data-stu-id="d13d6-111">Pointer to the size of the reply APDU message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d13d6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d13d6-112">Return value</span></span>

<span data-ttu-id="d13d6-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d13d6-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d13d6-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d13d6-114">Return code</span></span>                                                                                   | <span data-ttu-id="d13d6-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d13d6-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d13d6-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d13d6-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d13d6-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="d13d6-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d13d6-119">Der *plsize* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d13d6-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d13d6-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d13d6-121">Es wurde ein fehlerhafter Zeiger an *plsize* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d13d6-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="d13d6-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d13d6-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d13d6-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d13d6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d13d6-124">Remarks</span></span>

<span data-ttu-id="d13d6-125">Um ein vorhandenes Antwort-APDU abzurufen, nennen [**Sie get \_ apdureply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="d13d6-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="d13d6-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d13d6-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d13d6-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d13d6-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d13d6-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d13d6-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d13d6-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d13d6-129">Examples</span></span>

<span data-ttu-id="d13d6-130">Im folgenden Beispiel wird gezeigt, wie die Länge der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d13d6-130">The following example shows how to retrieve the length of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="d13d6-131">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="d13d6-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="d13d6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d13d6-132">Requirements</span></span>



| <span data-ttu-id="d13d6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d13d6-133">Requirement</span></span> | <span data-ttu-id="d13d6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d13d6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d13d6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d13d6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d13d6-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d13d6-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d13d6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d13d6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d13d6-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d13d6-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d13d6-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d13d6-139">End of client support</span></span><br/>    | <span data-ttu-id="d13d6-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d13d6-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d13d6-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d13d6-141">End of server support</span></span><br/>    | <span data-ttu-id="d13d6-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d13d6-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d13d6-143">Header</span><span class="sxs-lookup"><span data-stu-id="d13d6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d13d6-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d13d6-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d13d6-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="d13d6-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d13d6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d13d6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d13d6-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d13d6-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d13d6-149">IID</span><span class="sxs-lookup"><span data-stu-id="d13d6-149">IID</span></span><br/>                      | <span data-ttu-id="d13d6-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="d13d6-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d13d6-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d13d6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d13d6-152">**\_apdureply erhalten**</span><span class="sxs-lookup"><span data-stu-id="d13d6-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="d13d6-153">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="d13d6-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="d13d6-154">**\_apdureply einfügen**</span><span class="sxs-lookup"><span data-stu-id="d13d6-154">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
