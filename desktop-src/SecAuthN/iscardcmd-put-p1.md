---
description: Legt den ersten Parameter (P1) der Anwendungsprotokoll (Application Protocol Data Unit, APDU) fest.
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: Iscardcmd::p ut_P1-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363588"
---
# <a name="iscardcmdput_p1-method"></a><span data-ttu-id="cc022-103">Iscardcmd::p UT \_ P1-Methode</span><span class="sxs-lookup"><span data-stu-id="cc022-103">ISCardCmd::put\_P1 method</span></span>

<span data-ttu-id="cc022-104">\[Die **Put \_ P1** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cc022-104">\[The **put\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cc022-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc022-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cc022-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="cc022-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cc022-107">Die **Put \_ P1** -Methode legt das erste Parameter-Byte (P1) der [*Anwendungsprotokoll Dateneinheit*](../secgloss/a-gly.md) (APDU) fest.</span><span class="sxs-lookup"><span data-stu-id="cc022-107">The **put\_P1** method sets the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc022-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc022-108">Syntax</span></span>


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a><span data-ttu-id="cc022-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc022-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc022-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc022-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc022-111">Das Byte, das das P1-Feld ist.</span><span class="sxs-lookup"><span data-stu-id="cc022-111">The byte that is the P1 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc022-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc022-112">Return value</span></span>

<span data-ttu-id="cc022-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cc022-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cc022-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cc022-114">Return code</span></span>                                                                                   | <span data-ttu-id="cc022-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc022-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="cc022-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc022-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cc022-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cc022-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="cc022-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="cc022-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cc022-119">Der *byP1* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cc022-119">The *byP1* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="cc022-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cc022-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cc022-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc022-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="cc022-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc022-122">Remarks</span></span>

<span data-ttu-id="cc022-123">Um den P2-Wert des APDU festzulegen, nennen [**Sie get \_ P2**](iscardcmd-get-p2.md).</span><span class="sxs-lookup"><span data-stu-id="cc022-123">To set the P2 value of the APDU, call [**get\_P2**](iscardcmd-get-p2.md).</span></span>

<span data-ttu-id="cc022-124">Um die vorhandenen Werte für P1, P2 und P3 abzurufen, rufen [**Sie get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) oder [**get \_ P3**](iscardcmd-get-p3.md) auf.</span><span class="sxs-lookup"><span data-stu-id="cc022-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="cc022-125">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="cc022-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="cc022-126">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cc022-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cc022-127">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cc022-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cc022-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc022-128">Examples</span></span>

<span data-ttu-id="cc022-129">Im folgenden Beispiel wird gezeigt, wie Sie das erste Parameter-Byte (P1) der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) festlegen.</span><span class="sxs-lookup"><span data-stu-id="cc022-129">The following example shows how to set the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="cc022-130">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="cc022-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="cc022-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc022-131">Requirements</span></span>



| <span data-ttu-id="cc022-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc022-132">Requirement</span></span> | <span data-ttu-id="cc022-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cc022-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc022-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc022-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cc022-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc022-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cc022-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc022-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cc022-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc022-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc022-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cc022-138">End of client support</span></span><br/>    | <span data-ttu-id="cc022-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc022-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cc022-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cc022-140">End of server support</span></span><br/>    | <span data-ttu-id="cc022-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc022-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cc022-142">Header</span><span class="sxs-lookup"><span data-stu-id="cc022-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc022-143"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cc022-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc022-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cc022-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc022-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cc022-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cc022-146">DLL</span><span class="sxs-lookup"><span data-stu-id="cc022-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc022-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc022-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cc022-148">IID</span><span class="sxs-lookup"><span data-stu-id="cc022-148">IID</span></span><br/>                      | <span data-ttu-id="cc022-149">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="cc022-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="cc022-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc022-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc022-151">**\_P1 erhalten**</span><span class="sxs-lookup"><span data-stu-id="cc022-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="cc022-152">**\_P2 erhalten**</span><span class="sxs-lookup"><span data-stu-id="cc022-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="cc022-153">**\_P3 erhalten**</span><span class="sxs-lookup"><span data-stu-id="cc022-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="cc022-154">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="cc022-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="cc022-155">**\_P2 platzieren**</span><span class="sxs-lookup"><span data-stu-id="cc022-155">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
