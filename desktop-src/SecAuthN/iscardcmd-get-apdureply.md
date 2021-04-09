---
description: Ruft die Antwort-APDU ab und platziert Sie in einem bestimmten Byte Puffer.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Iscardcmd:: get_ApduReply-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050564"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="2ede6-103">Iscardcmd:: get \_ apdureply-Methode</span><span class="sxs-lookup"><span data-stu-id="2ede6-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="2ede6-104">\[Die Methode " **get \_ apdureply** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2ede6-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2ede6-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ede6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ede6-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2ede6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2ede6-107">Die **get \_ apdureply** -Methode ruft die [*Antwort-APDU*](../secgloss/r-gly.md)ab und platziert Sie in einem bestimmten Byte Puffer.</span><span class="sxs-lookup"><span data-stu-id="2ede6-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="2ede6-108">Die Antwort kann **null** sein, wenn keine [*Transaktion*](../secgloss/t-gly.md) für den Befehl APDU ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ede6-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ede6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ede6-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="2ede6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ede6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ede6-111">*ppreplyapdu* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2ede6-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ede6-112">Zeiger auf den Byte Puffer (durch ein **IStream** -Objekt zugeordnet), der die APDU-Antwortnachricht bei Rückgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="2ede6-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ede6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ede6-113">Return value</span></span>

<span data-ttu-id="2ede6-114">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="2ede6-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2ede6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2ede6-115">Return code</span></span>                                                                                   | <span data-ttu-id="2ede6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ede6-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="2ede6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ede6-118">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2ede6-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="2ede6-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2ede6-120">Der *ppreplyapdu* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2ede6-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="2ede6-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2ede6-122">Ein fehlerhafter Zeiger wurde in " *ppreplyapdu*" übergeben.</span><span class="sxs-lookup"><span data-stu-id="2ede6-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="2ede6-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ede6-124">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2ede6-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="2ede6-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ede6-125">Remarks</span></span>

<span data-ttu-id="2ede6-126">Um die Länge der APDU-Antwort zu ermitteln, wenden [**Sie sich an get \_ apdureplylength**](iscardcmd-get-apdureplylength.md).</span><span class="sxs-lookup"><span data-stu-id="2ede6-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="2ede6-127">Um einen neuen Antwort-APDU festzulegen, wenden Sie [**Put \_ apdureply**](iscardcmd-put-apdureply.md)an.</span><span class="sxs-lookup"><span data-stu-id="2ede6-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="2ede6-128">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="2ede6-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="2ede6-129">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2ede6-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2ede6-130">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2ede6-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2ede6-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ede6-131">Examples</span></span>

<span data-ttu-id="2ede6-132">Im folgenden Beispiel wird gezeigt, wie Antwortdaten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2ede6-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="2ede6-133">Im Beispiel wird davon ausgegangen, dass lLe eine Variable vom Typ **Long** ist, deren Wert durch einen vorherigen Aufrufen der [**iscardcmd:: get \_ apdureplylength**](iscardcmd-get-apdureplylength.md) -Methode festgelegt wurde, dass pibytereply ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist und dass der Wert von piscardcmd ein gültiger Zeiger auf eine Instanz der [**iscardc**](iscardcmd.md)</span><span class="sxs-lookup"><span data-stu-id="2ede6-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="2ede6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ede6-134">Requirements</span></span>



| <span data-ttu-id="2ede6-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ede6-135">Requirement</span></span> | <span data-ttu-id="2ede6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2ede6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ede6-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ede6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2ede6-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ede6-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2ede6-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ede6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2ede6-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ede6-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ede6-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2ede6-141">End of client support</span></span><br/>    | <span data-ttu-id="2ede6-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ede6-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2ede6-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="2ede6-143">End of server support</span></span><br/>    | <span data-ttu-id="2ede6-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ede6-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2ede6-145">Header</span><span class="sxs-lookup"><span data-stu-id="2ede6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ede6-146"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ede6-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2ede6-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ede6-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ede6-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2ede6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ede6-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ede6-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2ede6-151">IID</span><span class="sxs-lookup"><span data-stu-id="2ede6-151">IID</span></span><br/>                      | <span data-ttu-id="2ede6-152">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="2ede6-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2ede6-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ede6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ede6-154">**\_apdureplylength erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ede6-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="2ede6-155">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="2ede6-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="2ede6-156">**\_apdureply einfügen**</span><span class="sxs-lookup"><span data-stu-id="2ede6-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
