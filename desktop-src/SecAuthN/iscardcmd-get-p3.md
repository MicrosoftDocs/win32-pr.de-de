---
description: Ruft den dritten Parameter (P3) aus der Anwendungsprotokoll Dateneinheit (APDU) ab.
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Iscardcmd:: get_P3-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129340"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="060a8-103">Iscardcmd:: get \_ P3-Methode</span><span class="sxs-lookup"><span data-stu-id="060a8-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="060a8-104">\[Die **get \_ P3** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="060a8-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="060a8-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="060a8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="060a8-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="060a8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="060a8-107">Die **get \_ P3** -Methode ruft den dritten Parameter (P3) aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) ab.</span><span class="sxs-lookup"><span data-stu-id="060a8-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="060a8-108">Dieser schreibgeschützte Bytewert stellt die Größe des Datentyps des APDU dar.</span><span class="sxs-lookup"><span data-stu-id="060a8-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="060a8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="060a8-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="060a8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="060a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060a8-111">*pbyP3* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="060a8-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060a8-112">Zeiger auf das Byte, das bei der Rückgabe aus dem APDU P3 ist.</span><span class="sxs-lookup"><span data-stu-id="060a8-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060a8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="060a8-113">Return value</span></span>

<span data-ttu-id="060a8-114">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="060a8-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="060a8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="060a8-115">Return code</span></span>                                                                                   | <span data-ttu-id="060a8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="060a8-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="060a8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="060a8-118">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="060a8-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="060a8-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="060a8-120">Der *pbyP3* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="060a8-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="060a8-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="060a8-122">In *pbyP3* wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="060a8-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="060a8-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="060a8-124">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="060a8-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="060a8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="060a8-125">Remarks</span></span>

<span data-ttu-id="060a8-126">Der P3-Parameter ist schreibgeschützt und kann daher nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="060a8-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="060a8-127">Zum Abrufen der Parameter "P1" oder "P2" müssen [**Sie get \_ P1**](iscardcmd-get-p1.md) bzw. [**\_ P2**](iscardcmd-get-p2.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="060a8-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="060a8-128">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="060a8-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="060a8-129">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="060a8-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="060a8-130">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="060a8-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="060a8-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="060a8-131">Examples</span></span>

<span data-ttu-id="060a8-132">Im folgenden Beispiel wird gezeigt, wie das dritte Parameter-Byte (P3) aus der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="060a8-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="060a8-133">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="060a8-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="060a8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="060a8-134">Requirements</span></span>



| <span data-ttu-id="060a8-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="060a8-135">Requirement</span></span> | <span data-ttu-id="060a8-136">Wert</span><span class="sxs-lookup"><span data-stu-id="060a8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="060a8-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="060a8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="060a8-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="060a8-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="060a8-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="060a8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="060a8-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="060a8-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="060a8-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="060a8-141">End of client support</span></span><br/>    | <span data-ttu-id="060a8-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="060a8-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="060a8-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="060a8-143">End of server support</span></span><br/>    | <span data-ttu-id="060a8-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="060a8-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="060a8-145">Header</span><span class="sxs-lookup"><span data-stu-id="060a8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="060a8-146"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="060a8-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="060a8-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="060a8-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="060a8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="060a8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="060a8-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="060a8-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="060a8-151">IID</span><span class="sxs-lookup"><span data-stu-id="060a8-151">IID</span></span><br/>                      | <span data-ttu-id="060a8-152">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="060a8-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="060a8-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="060a8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060a8-154">**\_P1 erhalten**</span><span class="sxs-lookup"><span data-stu-id="060a8-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="060a8-155">**\_P2 erhalten**</span><span class="sxs-lookup"><span data-stu-id="060a8-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="060a8-156">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="060a8-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
