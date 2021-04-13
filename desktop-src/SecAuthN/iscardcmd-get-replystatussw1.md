---
description: Ruft das Antwort-APDUs SW1 Status Byte ab.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'Iscardcmd:: get_ReplyStatusSW1-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526351"
---
# <a name="iscardcmdget_replystatussw1-method"></a><span data-ttu-id="1ddd1-103">Iscardcmd:: get \_ ReplyStatusSW1-Methode</span><span class="sxs-lookup"><span data-stu-id="1ddd1-103">ISCardCmd::get\_ReplyStatusSW1 method</span></span>

<span data-ttu-id="1ddd1-104">\[Die Methode " **get \_ ReplyStatusSW1** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-104">\[The **get\_ReplyStatusSW1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ddd1-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1ddd1-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1ddd1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1ddd1-107">Die **get \_ ReplyStatusSW1** -Methode ruft das [*Antwort-APDUs*](../secgloss/r-gly.md) SW1 Status Byte ab.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-107">The **get\_ReplyStatusSW1** method retrieves the [*reply APDUs*](../secgloss/r-gly.md) SW1 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddd1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ddd1-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a><span data-ttu-id="1ddd1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ddd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ddd1-110">*pbySW1* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1ddd1-110">*pbySW1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ddd1-111">Zeiger auf das Byte, das den Wert des SW1 Byte bei der Rückgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-111">Pointer to the byte that contains the value of the SW1 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ddd1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ddd1-112">Return value</span></span>

<span data-ttu-id="1ddd1-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1ddd1-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1ddd1-114">Return code</span></span>                                                                                   | <span data-ttu-id="1ddd1-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ddd1-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1ddd1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1ddd1-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="1ddd1-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1ddd1-119">Der *pbySW1* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-119">The *pbySW1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="1ddd1-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1ddd1-121">In *pbySW1* wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-121">A bad pointer was passed in *pbySW1*.</span></span><br/> |
| <dl> <span data-ttu-id="1ddd1-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1ddd1-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="1ddd1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ddd1-124">Remarks</span></span>

<span data-ttu-id="1ddd1-125">Das SW1-Status Byte der [*Antwort APDU*](../secgloss/r-gly.md) ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-125">The [*reply APDU's*](../secgloss/r-gly.md) SW1 status byte is read-only.</span></span>

<span data-ttu-id="1ddd1-126">Rufen [**Sie get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)auf, um das SW2-Status Byte der Antwort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-126">To retrieve the reply APDU's SW2 status byte, call [**get\_ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span></span>

<span data-ttu-id="1ddd1-127">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="1ddd1-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="1ddd1-128">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1ddd1-129">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1ddd1-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1ddd1-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ddd1-130">Examples</span></span>

<span data-ttu-id="1ddd1-131">Im folgenden Beispiel wird gezeigt, wie das SW1-Status Byte der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-131">The following example shows how to retrieve the SW1 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="1ddd1-132">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="1ddd1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ddd1-133">Requirements</span></span>



| <span data-ttu-id="1ddd1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ddd1-134">Requirement</span></span> | <span data-ttu-id="1ddd1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1ddd1-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddd1-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ddd1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1ddd1-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ddd1-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1ddd1-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ddd1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1ddd1-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ddd1-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ddd1-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1ddd1-140">End of client support</span></span><br/>    | <span data-ttu-id="1ddd1-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ddd1-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1ddd1-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1ddd1-142">End of server support</span></span><br/>    | <span data-ttu-id="1ddd1-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ddd1-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1ddd1-144">Header</span><span class="sxs-lookup"><span data-stu-id="1ddd1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ddd1-145"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ddd1-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1ddd1-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="1ddd1-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1ddd1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1ddd1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ddd1-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ddd1-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1ddd1-150">IID</span><span class="sxs-lookup"><span data-stu-id="1ddd1-150">IID</span></span><br/>                      | <span data-ttu-id="1ddd1-151">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="1ddd1-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1ddd1-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ddd1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ddd1-153">**get \_ ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="1ddd1-153">**get\_ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[<span data-ttu-id="1ddd1-154">**\_replystatus erhalten**</span><span class="sxs-lookup"><span data-stu-id="1ddd1-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="1ddd1-155">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="1ddd1-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
