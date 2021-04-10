---
description: Ruft das Nachrichten Status Wort von APDU ab.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'Iscardcmd:: get_ReplyStatus-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129333"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="fb307-103">Iscardcmd:: get \_ replystatus-Methode</span><span class="sxs-lookup"><span data-stu-id="fb307-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="fb307-104">\[Die **get \_ replystatus** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fb307-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb307-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb307-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb307-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fb307-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fb307-107">Die **get \_ replystatus** -Methode ruft das Nachrichten Status Wort [*von APDU*](../secgloss/r-gly.md) ab.</span><span class="sxs-lookup"><span data-stu-id="fb307-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb307-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb307-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fb307-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb307-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb307-110">*pwstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb307-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb307-111">Zeiger auf das Wort, das den Status bei der Rückgabe hat.</span><span class="sxs-lookup"><span data-stu-id="fb307-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb307-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb307-112">Return value</span></span>

<span data-ttu-id="fb307-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="fb307-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fb307-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fb307-114">Return code</span></span>                                                                                   | <span data-ttu-id="fb307-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb307-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="fb307-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb307-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fb307-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="fb307-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fb307-119">Der *pwstatus* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="fb307-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fb307-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fb307-121">Ein fehlerhafter Zeiger wurde in *pwstatus* übergeben.</span><span class="sxs-lookup"><span data-stu-id="fb307-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="fb307-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb307-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fb307-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="fb307-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb307-124">Remarks</span></span>

<span data-ttu-id="fb307-125">Um das Nachrichten Status Wort für die Antwort APDU festzulegen, wenden Sie [**Put \_ replystatus**](iscardcmd-put-replystatus.md)an.</span><span class="sxs-lookup"><span data-stu-id="fb307-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="fb307-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="fb307-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="fb307-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fb307-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fb307-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fb307-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fb307-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb307-129">Examples</span></span>

<span data-ttu-id="fb307-130">Im folgenden Beispiel wird gezeigt, wie das Nachrichten Status Wort der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fb307-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="fb307-131">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="fb307-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="fb307-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb307-132">Requirements</span></span>



| <span data-ttu-id="fb307-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb307-133">Requirement</span></span> | <span data-ttu-id="fb307-134">Wert</span><span class="sxs-lookup"><span data-stu-id="fb307-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb307-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb307-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fb307-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb307-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fb307-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb307-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fb307-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb307-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb307-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fb307-139">End of client support</span></span><br/>    | <span data-ttu-id="fb307-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb307-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fb307-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="fb307-141">End of server support</span></span><br/>    | <span data-ttu-id="fb307-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb307-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fb307-143">Header</span><span class="sxs-lookup"><span data-stu-id="fb307-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb307-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb307-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fb307-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb307-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb307-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fb307-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb307-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb307-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb307-149">IID</span><span class="sxs-lookup"><span data-stu-id="fb307-149">IID</span></span><br/>                      | <span data-ttu-id="fb307-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="fb307-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fb307-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb307-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb307-152">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="fb307-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="fb307-153">**Put \_ replystatus**</span><span class="sxs-lookup"><span data-stu-id="fb307-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
