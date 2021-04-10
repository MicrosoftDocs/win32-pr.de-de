---
description: Legt den zweiten Parameter (P2) in der Application Protocol Data Unit (APDU) fest.
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: Iscardcmd::p ut_P2-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214407"
---
# <a name="iscardcmdput_p2-method"></a><span data-ttu-id="6c262-103">Iscardcmd::p UT \_ P2-Methode</span><span class="sxs-lookup"><span data-stu-id="6c262-103">ISCardCmd::put\_P2 method</span></span>

<span data-ttu-id="6c262-104">\[Die **Put \_ P2** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6c262-104">\[The **put\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c262-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c262-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6c262-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6c262-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6c262-107">Mit der **Put \_ P2** -Methode wird der zweite Parameter (P2) in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c262-107">The **put\_P2** method sets the second parameter (P2) byte in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c262-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c262-108">Syntax</span></span>


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a><span data-ttu-id="6c262-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c262-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c262-110">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c262-110">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c262-111">Das Byte, das das P2-Feld ist.</span><span class="sxs-lookup"><span data-stu-id="6c262-111">The byte that is the P2 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c262-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c262-112">Return value</span></span>

<span data-ttu-id="6c262-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6c262-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6c262-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c262-114">Return code</span></span>                                                                                   | <span data-ttu-id="6c262-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c262-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="6c262-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c262-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6c262-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6c262-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="6c262-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6c262-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6c262-119">Der *byP2* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c262-119">The *byP2* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6c262-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6c262-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6c262-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6c262-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6c262-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c262-122">Remarks</span></span>

<span data-ttu-id="6c262-123">Um den P1-Wert des APDU festzulegen, nennen Sie [**Put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="6c262-123">To set the P1 value of the APDU, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="6c262-124">Um die vorhandenen Werte für P1, P2 und P3 abzurufen, rufen [**Sie get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) oder [**get \_ P3**](iscardcmd-get-p3.md) auf.</span><span class="sxs-lookup"><span data-stu-id="6c262-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="6c262-125">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="6c262-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="6c262-126">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6c262-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6c262-127">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6c262-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c262-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c262-128">Examples</span></span>

<span data-ttu-id="6c262-129">Im folgenden Beispiel wird gezeigt, wie Sie das zweite Parameter-Byte (P2) der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) festlegen.</span><span class="sxs-lookup"><span data-stu-id="6c262-129">The following example shows how to set the second parameter (P2) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="6c262-130">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="6c262-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6c262-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c262-131">Requirements</span></span>



| <span data-ttu-id="6c262-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c262-132">Requirement</span></span> | <span data-ttu-id="6c262-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6c262-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c262-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c262-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6c262-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c262-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6c262-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c262-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6c262-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c262-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c262-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6c262-138">End of client support</span></span><br/>    | <span data-ttu-id="6c262-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c262-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6c262-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6c262-140">End of server support</span></span><br/>    | <span data-ttu-id="6c262-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c262-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6c262-142">Header</span><span class="sxs-lookup"><span data-stu-id="6c262-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c262-143"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6c262-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c262-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6c262-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c262-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c262-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c262-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6c262-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c262-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c262-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c262-148">IID</span><span class="sxs-lookup"><span data-stu-id="6c262-148">IID</span></span><br/>                      | <span data-ttu-id="6c262-149">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="6c262-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6c262-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c262-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c262-151">**\_P1 erhalten**</span><span class="sxs-lookup"><span data-stu-id="6c262-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="6c262-152">**\_P2 erhalten**</span><span class="sxs-lookup"><span data-stu-id="6c262-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="6c262-153">**\_P3 erhalten**</span><span class="sxs-lookup"><span data-stu-id="6c262-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="6c262-154">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="6c262-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="6c262-155">**\_P1 platzieren**</span><span class="sxs-lookup"><span data-stu-id="6c262-155">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
