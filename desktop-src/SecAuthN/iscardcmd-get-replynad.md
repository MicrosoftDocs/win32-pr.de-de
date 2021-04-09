---
description: Ruft die von der Smartcard verwendete Knotenadresse (nad) in der Antwortnachricht ab.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Iscardcmd:: get_ReplyNad-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129336"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="497fb-103">Iscardcmd:: get \_ replynad-Methode</span><span class="sxs-lookup"><span data-stu-id="497fb-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="497fb-104">\[Die **get \_ replynad** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="497fb-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="497fb-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="497fb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="497fb-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="497fb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="497fb-107">Die **get \_ replynad** -Methode ruft die von der [*Smartcard*](../secgloss/s-gly.md) verwendete Knotenadresse (nad) in der Antwortnachricht ab.</span><span class="sxs-lookup"><span data-stu-id="497fb-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="497fb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="497fb-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="497fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="497fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497fb-110">*pbnad* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="497fb-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="497fb-111">Zeiger auf das Byte, das das von der Antwortnachricht verwendete nad bei der Rückgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="497fb-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497fb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="497fb-112">Return value</span></span>

<span data-ttu-id="497fb-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="497fb-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="497fb-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="497fb-114">Return code</span></span>                                                                                    | <span data-ttu-id="497fb-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="497fb-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="497fb-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="497fb-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="497fb-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="497fb-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="497fb-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="497fb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="497fb-119">Der *pbnad* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="497fb-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="497fb-120"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="497fb-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="497fb-121">Bei internen aufrufen konnten die nad-Informationen nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="497fb-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="497fb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="497fb-122">Remarks</span></span>

<span data-ttu-id="497fb-123">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Methode möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="497fb-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="497fb-124">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="497fb-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="497fb-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="497fb-125">Examples</span></span>

<span data-ttu-id="497fb-126">Im folgenden Beispiel wird gezeigt, wie die von der [*Smartcard*](../secgloss/s-gly.md) verwendete Knotenadresse (nad) in der Antwortnachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="497fb-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="497fb-127">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="497fb-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="497fb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="497fb-128">Requirements</span></span>



| <span data-ttu-id="497fb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="497fb-129">Requirement</span></span> | <span data-ttu-id="497fb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="497fb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="497fb-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="497fb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="497fb-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="497fb-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="497fb-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="497fb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="497fb-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="497fb-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="497fb-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="497fb-135">End of client support</span></span><br/>    | <span data-ttu-id="497fb-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="497fb-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="497fb-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="497fb-137">End of server support</span></span><br/>    | <span data-ttu-id="497fb-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="497fb-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="497fb-139">Header</span><span class="sxs-lookup"><span data-stu-id="497fb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="497fb-140"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="497fb-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="497fb-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="497fb-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="497fb-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="497fb-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="497fb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="497fb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="497fb-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="497fb-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="497fb-145">IID</span><span class="sxs-lookup"><span data-stu-id="497fb-145">IID</span></span><br/>                      | <span data-ttu-id="497fb-146">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="497fb-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="497fb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="497fb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497fb-148">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="497fb-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
