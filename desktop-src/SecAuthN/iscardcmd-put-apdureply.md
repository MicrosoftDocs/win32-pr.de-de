---
description: Legt eine neue Antwort-APDU fest.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: Iscardcmd::p ut_ApduReply-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862635"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="2f4aa-103">Iscardcmd::p UT- \_ apdureply-Methode</span><span class="sxs-lookup"><span data-stu-id="2f4aa-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="2f4aa-104">\[Die **Put \_ apdureply** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f4aa-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f4aa-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2f4aa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2f4aa-107">Mit der **Put \_ apdureply** -Methode wird eine neue [*Antwort-APDU*](../secgloss/r-gly.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f4aa-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="2f4aa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f4aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4aa-110">*preplyapdu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f4aa-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4aa-111">Ein Zeiger auf den Byte Puffer (durch ein **IStream** -Objekt zugeordnet), der bei der Rückgabe die APDU-Wiedergabe Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4aa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f4aa-112">Return value</span></span>

<span data-ttu-id="2f4aa-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2f4aa-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2f4aa-114">Return code</span></span>                                                                                   | <span data-ttu-id="2f4aa-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f4aa-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2f4aa-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2f4aa-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="2f4aa-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2f4aa-119">Der *preplyapdu* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="2f4aa-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2f4aa-121">Ein fehlerhafter Zeiger wurde in *preplyapdu* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="2f4aa-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2f4aa-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="2f4aa-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f4aa-124">Remarks</span></span>

<span data-ttu-id="2f4aa-125">Um ein vorhandenes Antwort-APDU abzurufen, nennen [**Sie get \_ apdureply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="2f4aa-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="2f4aa-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="2f4aa-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="2f4aa-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2f4aa-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2f4aa-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2f4aa-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f4aa-129">Examples</span></span>

<span data-ttu-id="2f4aa-130">Im folgenden Beispiel wird gezeigt, wie ein neues [*Antwort-APDU*](../secgloss/r-gly.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="2f4aa-131">In diesem Beispiel wird davon ausgegangen, dass pibytereply ein gültiger Zeiger auf eine Instanz von [**ibytebuffer**](ibytebuffer.md)ist und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="2f4aa-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f4aa-132">Requirements</span></span>



| <span data-ttu-id="2f4aa-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f4aa-133">Requirement</span></span> | <span data-ttu-id="2f4aa-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2f4aa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4aa-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4aa-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f4aa-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f4aa-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4aa-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f4aa-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f4aa-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-139">End of client support</span></span><br/>    | <span data-ttu-id="2f4aa-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f4aa-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2f4aa-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-141">End of server support</span></span><br/>    | <span data-ttu-id="2f4aa-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f4aa-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2f4aa-143">Header</span><span class="sxs-lookup"><span data-stu-id="2f4aa-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f4aa-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f4aa-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2f4aa-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f4aa-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f4aa-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2f4aa-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f4aa-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f4aa-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f4aa-149">IID</span><span class="sxs-lookup"><span data-stu-id="2f4aa-149">IID</span></span><br/>                      | <span data-ttu-id="2f4aa-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2f4aa-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f4aa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4aa-152">**\_apdureply erhalten**</span><span class="sxs-lookup"><span data-stu-id="2f4aa-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="2f4aa-153">**\_apdureplylength erhalten**</span><span class="sxs-lookup"><span data-stu-id="2f4aa-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="2f4aa-154">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="2f4aa-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
