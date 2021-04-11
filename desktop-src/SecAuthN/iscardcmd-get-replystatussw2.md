---
description: Ruft das Antwort-APDU-SW2 Status Byte ab.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'Iscardcmd:: get_ReplyStatusSW2-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129332"
---
# <a name="iscardcmdget_replystatussw2-method"></a><span data-ttu-id="a9139-103">Iscardcmd:: get \_ ReplyStatusSW2-Methode</span><span class="sxs-lookup"><span data-stu-id="a9139-103">ISCardCmd::get\_ReplyStatusSW2 method</span></span>

<span data-ttu-id="a9139-104">\[Die Methode " **get \_ ReplyStatusSW2** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a9139-104">\[The **get\_ReplyStatusSW2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a9139-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9139-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9139-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a9139-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a9139-107">Die **get \_ ReplyStatusSW2** -Methode ruft die [*Antwort APDU*](../secgloss/r-gly.md) SW2 Status Byte ab.</span><span class="sxs-lookup"><span data-stu-id="a9139-107">The **get\_ReplyStatusSW2** method retrieves the [*reply APDU*](../secgloss/r-gly.md) SW2 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9139-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9139-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a><span data-ttu-id="a9139-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9139-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9139-110">*pbySW2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a9139-110">*pbySW2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9139-111">Zeiger auf das Byte, das den Wert des SW2 Byte bei der Rückgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="a9139-111">Pointer to the byte that contains the value of the SW2 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9139-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9139-112">Return value</span></span>

<span data-ttu-id="a9139-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a9139-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a9139-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a9139-114">Return code</span></span>                                                                                   | <span data-ttu-id="a9139-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9139-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a9139-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a9139-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a9139-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a9139-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a9139-119">Der *pbySW2* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a9139-119">The *pbySW2* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="a9139-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a9139-121">In *pbySW2* wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a9139-121">A bad pointer was passed in *pbySW2*.</span></span><br/> |
| <dl> <span data-ttu-id="a9139-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a9139-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a9139-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a9139-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9139-124">Remarks</span></span>

<span data-ttu-id="a9139-125">Das SW2-Status Byte der Antwort APDU ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a9139-125">The reply APDU's SW2 status byte is read-only.</span></span>

<span data-ttu-id="a9139-126">Rufen [**Sie get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)auf, um das SW1-Status Byte der Antwort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a9139-126">To retrieve the reply APDU's SW1 status byte, call [**get\_ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span></span>

<span data-ttu-id="a9139-127">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a9139-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a9139-128">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a9139-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a9139-129">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a9139-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a9139-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9139-130">Examples</span></span>

<span data-ttu-id="a9139-131">Im folgenden Beispiel wird gezeigt, wie das SW2-Status Byte der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a9139-131">The following example shows how to retrieve the SW2 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="a9139-132">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="a9139-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a9139-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9139-133">Requirements</span></span>



| <span data-ttu-id="a9139-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9139-134">Requirement</span></span> | <span data-ttu-id="a9139-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a9139-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9139-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9139-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a9139-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9139-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9139-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9139-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a9139-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9139-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9139-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a9139-140">End of client support</span></span><br/>    | <span data-ttu-id="a9139-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9139-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a9139-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a9139-142">End of server support</span></span><br/>    | <span data-ttu-id="a9139-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9139-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a9139-144">Header</span><span class="sxs-lookup"><span data-stu-id="a9139-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9139-145"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9139-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a9139-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9139-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a9139-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a9139-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9139-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9139-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9139-150">IID</span><span class="sxs-lookup"><span data-stu-id="a9139-150">IID</span></span><br/>                      | <span data-ttu-id="a9139-151">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="a9139-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a9139-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9139-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9139-153">**get \_ ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="a9139-153">**get\_ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[<span data-ttu-id="a9139-154">**\_replystatus erhalten**</span><span class="sxs-lookup"><span data-stu-id="a9139-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="a9139-155">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="a9139-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
