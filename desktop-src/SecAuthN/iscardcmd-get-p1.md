---
description: Ruft den ersten Parameter (P1) aus der Anwendungsprotokoll Dateneinheit (APDU) ab.
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'Iscardcmd:: get_P1-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 047732fd8602828cc0501d623c57653bfdc9044f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526354"
---
# <a name="iscardcmdget_p1-method"></a><span data-ttu-id="1aae5-103">Iscardcmd:: get \_ P1-Methode</span><span class="sxs-lookup"><span data-stu-id="1aae5-103">ISCardCmd::get\_P1 method</span></span>

<span data-ttu-id="1aae5-104">\[Die **get \_ P1** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1aae5-104">\[The **get\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1aae5-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1aae5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1aae5-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1aae5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1aae5-107">Die **get \_ P1** -Methode ruft den ersten Parameter (P1) aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) ab.</span><span class="sxs-lookup"><span data-stu-id="1aae5-107">The **get\_P1** method retrieves the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="1aae5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aae5-108">Syntax</span></span>


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a><span data-ttu-id="1aae5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aae5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aae5-110">*pbyP1* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1aae5-110">*pbyP1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aae5-111">Zeiger auf das P1-Byte in der APDU bei der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="1aae5-111">Pointer to the P1 byte in the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aae5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aae5-112">Return value</span></span>

<span data-ttu-id="1aae5-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1aae5-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1aae5-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1aae5-114">Return code</span></span>                                                                                   | <span data-ttu-id="1aae5-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1aae5-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1aae5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1aae5-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1aae5-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="1aae5-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1aae5-119">Der *pbyP1* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1aae5-119">The *pbyP1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="1aae5-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1aae5-121">In *pbyP1* wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1aae5-121">A bad pointer was passed in *pbyP1*.</span></span><br/> |
| <dl> <span data-ttu-id="1aae5-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1aae5-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1aae5-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="1aae5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aae5-124">Remarks</span></span>

<span data-ttu-id="1aae5-125">Um den P1-Parameter auf einen neuen Wert festzulegen, wenden Sie [**Put \_ P1**](iscardcmd-put-p1.md)an.</span><span class="sxs-lookup"><span data-stu-id="1aae5-125">To set the P1 parameter to a new value, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="1aae5-126">Zum Abrufen der P2-oder P3-Parameter müssen [**Sie get \_ P2**](iscardcmd-get-p2.md) und [**get \_**](iscardcmd-get-p3.md) P2 abrufen.</span><span class="sxs-lookup"><span data-stu-id="1aae5-126">To get the P2 or P3 parameters, call [**get\_P2**](iscardcmd-get-p2.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="1aae5-127">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="1aae5-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="1aae5-128">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1aae5-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1aae5-129">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1aae5-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1aae5-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1aae5-130">Examples</span></span>

<span data-ttu-id="1aae5-131">Im folgenden Beispiel wird gezeigt, wie der erste Parameter (P1) aus der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1aae5-131">The following example shows how to retrieve the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="1aae5-132">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="1aae5-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="1aae5-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aae5-133">Requirements</span></span>



| <span data-ttu-id="1aae5-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aae5-134">Requirement</span></span> | <span data-ttu-id="1aae5-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1aae5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aae5-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1aae5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1aae5-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1aae5-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1aae5-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1aae5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1aae5-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1aae5-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1aae5-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1aae5-140">End of client support</span></span><br/>    | <span data-ttu-id="1aae5-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1aae5-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1aae5-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1aae5-142">End of server support</span></span><br/>    | <span data-ttu-id="1aae5-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1aae5-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1aae5-144">Header</span><span class="sxs-lookup"><span data-stu-id="1aae5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aae5-145"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1aae5-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1aae5-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="1aae5-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1aae5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1aae5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aae5-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aae5-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1aae5-150">IID</span><span class="sxs-lookup"><span data-stu-id="1aae5-150">IID</span></span><br/>                      | <span data-ttu-id="1aae5-151">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="1aae5-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1aae5-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aae5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aae5-153">**\_P2 erhalten**</span><span class="sxs-lookup"><span data-stu-id="1aae5-153">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="1aae5-154">**\_P3 erhalten**</span><span class="sxs-lookup"><span data-stu-id="1aae5-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="1aae5-155">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="1aae5-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="1aae5-156">**\_P1 platzieren**</span><span class="sxs-lookup"><span data-stu-id="1aae5-156">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
