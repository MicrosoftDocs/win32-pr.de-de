---
description: Legt einen neuen Antwort-APDU-Nachrichten Status Wort fest.
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: Iscardcmd::p ut_ReplyStatus-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 55e6de81cd7e2c98b527d0852ea31a25f8256c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128297"
---
# <a name="iscardcmdput_replystatus-method"></a><span data-ttu-id="55a1e-103">Iscardcmd::p UT \_ replystatus-Methode</span><span class="sxs-lookup"><span data-stu-id="55a1e-103">ISCardCmd::put\_ReplyStatus method</span></span>

<span data-ttu-id="55a1e-104">\[Die **Put \_ replystatus** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="55a1e-104">\[The **put\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55a1e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55a1e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55a1e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="55a1e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="55a1e-107">Mit der **Put \_ replystatus** -Methode wird ein neues [*Antwort-APDU*](../secgloss/r-gly.md) -Nachrichten Status Wort festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55a1e-107">The **put\_ReplyStatus** method sets a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a1e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="55a1e-108">Syntax</span></span>


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a><span data-ttu-id="55a1e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="55a1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a1e-110">*wstatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55a1e-110">*wStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a1e-111">Word, das den Status hat.</span><span class="sxs-lookup"><span data-stu-id="55a1e-111">Word that is the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a1e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55a1e-112">Return value</span></span>

<span data-ttu-id="55a1e-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="55a1e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="55a1e-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="55a1e-114">Return code</span></span>                                                                                   | <span data-ttu-id="55a1e-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55a1e-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="55a1e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55a1e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="55a1e-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="55a1e-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="55a1e-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="55a1e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="55a1e-119">Der *wstatus* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="55a1e-119">The *wStatus* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="55a1e-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="55a1e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="55a1e-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="55a1e-121">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="55a1e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55a1e-122">Remarks</span></span>

<span data-ttu-id="55a1e-123">Um das Nachrichten Status Wort von APDU zu erhalten, geben [**Sie get \_ replystatus**](iscardcmd-get-replystatus.md)an.</span><span class="sxs-lookup"><span data-stu-id="55a1e-123">To get the reply APDU's message status word, call [**get\_ReplyStatus**](iscardcmd-get-replystatus.md).</span></span>

<span data-ttu-id="55a1e-124">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="55a1e-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="55a1e-125">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="55a1e-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="55a1e-126">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="55a1e-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="55a1e-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55a1e-127">Examples</span></span>

<span data-ttu-id="55a1e-128">Im folgenden Beispiel wird gezeigt, wie ein neues [*APDU*](../secgloss/r-gly.md) -Nachrichten Status Wort festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="55a1e-128">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span> <span data-ttu-id="55a1e-129">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="55a1e-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="55a1e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a1e-130">Requirements</span></span>



| <span data-ttu-id="55a1e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a1e-131">Requirement</span></span> | <span data-ttu-id="55a1e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="55a1e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a1e-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55a1e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="55a1e-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a1e-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55a1e-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55a1e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="55a1e-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a1e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55a1e-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="55a1e-137">End of client support</span></span><br/>    | <span data-ttu-id="55a1e-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="55a1e-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="55a1e-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="55a1e-139">End of server support</span></span><br/>    | <span data-ttu-id="55a1e-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55a1e-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="55a1e-141">Header</span><span class="sxs-lookup"><span data-stu-id="55a1e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a1e-142"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="55a1e-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="55a1e-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="55a1e-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="55a1e-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55a1e-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55a1e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="55a1e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a1e-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a1e-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="55a1e-147">IID</span><span class="sxs-lookup"><span data-stu-id="55a1e-147">IID</span></span><br/>                      | <span data-ttu-id="55a1e-148">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="55a1e-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="55a1e-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a1e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a1e-150">**\_replystatus erhalten**</span><span class="sxs-lookup"><span data-stu-id="55a1e-150">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="55a1e-151">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="55a1e-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
