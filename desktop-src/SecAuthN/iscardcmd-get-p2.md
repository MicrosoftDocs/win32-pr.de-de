---
description: Ruft den zweiten Parameter (P2) aus der Anwendungsprotokoll Dateneinheit (APDU) ab.
ms.assetid: c719786f-0f50-472e-a92e-a64c333fc255
title: 'Iscardcmd:: get_P2-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7811ad3e42264477210830f340338d0786ed5547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129337"
---
# <a name="iscardcmdget_p2-method"></a><span data-ttu-id="c5563-103">Iscardcmd:: get \_ P2-Methode</span><span class="sxs-lookup"><span data-stu-id="c5563-103">ISCardCmd::get\_P2 method</span></span>

<span data-ttu-id="c5563-104">\[Die **get \_ P2** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c5563-104">\[The **get\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5563-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5563-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c5563-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c5563-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c5563-107">Die **get \_ P2** -Methode ruft den zweiten Parameter (P2) aus der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) ab.</span><span class="sxs-lookup"><span data-stu-id="c5563-107">The **get\_P2** method retrieves the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5563-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5563-108">Syntax</span></span>


```C++
HRESULT get_P2(
  [out] BYTE *pbyP2
);
```



## <a name="parameters"></a><span data-ttu-id="c5563-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5563-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5563-110">*pbyP2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5563-110">*pbyP2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5563-111">Zeiger auf das Byte, das P2 aus dem APDU bei der Rückgabe ist.</span><span class="sxs-lookup"><span data-stu-id="c5563-111">Pointer to the byte that is the P2 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5563-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5563-112">Return value</span></span>

<span data-ttu-id="c5563-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c5563-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c5563-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c5563-114">Return code</span></span>                                                                                   | <span data-ttu-id="c5563-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5563-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c5563-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c5563-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c5563-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="c5563-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c5563-119">Der *pbyP2* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5563-119">The *pbyP2* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c5563-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c5563-121">In *pbyP2* wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c5563-121">A bad pointer was passed in *pbyP2*.</span></span><br/> |
| <dl> <span data-ttu-id="c5563-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c5563-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c5563-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="c5563-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5563-124">Remarks</span></span>

<span data-ttu-id="c5563-125">Um den P2-Parameter auf einen neuen Wert festzulegen, nennen Sie [**Put \_ P2**](iscardcmd-put-p2.md).</span><span class="sxs-lookup"><span data-stu-id="c5563-125">To set the P2 parameter to a new value, call [**put\_P2**](iscardcmd-put-p2.md).</span></span>

<span data-ttu-id="c5563-126">Um die P1-oder P3-Parameter abzurufen, nennen [**Sie get \_ P1**](iscardcmd-get-p1.md) , und [**holen Sie sich den Befehl \_ P3**](iscardcmd-get-p3.md) .</span><span class="sxs-lookup"><span data-stu-id="c5563-126">To get the P1 or P3 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="c5563-127">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="c5563-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="c5563-128">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c5563-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c5563-129">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c5563-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c5563-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5563-130">Examples</span></span>

<span data-ttu-id="c5563-131">Im folgenden Beispiel wird gezeigt, wie Sie den zweiten Parameter (P2) aus der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abrufen können.</span><span class="sxs-lookup"><span data-stu-id="c5563-131">The following example shows how to retrieve the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="c5563-132">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="c5563-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP2;
HRESULT  hr;

// Retrieve the P2 byte.
hr = pISCardCmd->get_P2(&byP2);
if (FAILED(hr))
{
  printf("Failed get_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="c5563-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5563-133">Requirements</span></span>



| <span data-ttu-id="c5563-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5563-134">Requirement</span></span> | <span data-ttu-id="c5563-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c5563-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5563-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5563-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c5563-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5563-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c5563-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5563-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c5563-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5563-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5563-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c5563-140">End of client support</span></span><br/>    | <span data-ttu-id="c5563-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5563-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c5563-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c5563-142">End of server support</span></span><br/>    | <span data-ttu-id="c5563-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5563-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c5563-144">Header</span><span class="sxs-lookup"><span data-stu-id="c5563-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5563-145"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5563-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c5563-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5563-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5563-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c5563-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5563-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5563-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5563-150">IID</span><span class="sxs-lookup"><span data-stu-id="c5563-150">IID</span></span><br/>                      | <span data-ttu-id="c5563-151">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="c5563-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c5563-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5563-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5563-153">**\_P1 erhalten**</span><span class="sxs-lookup"><span data-stu-id="c5563-153">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="c5563-154">**\_P3 erhalten**</span><span class="sxs-lookup"><span data-stu-id="c5563-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="c5563-155">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="c5563-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="c5563-156">**\_P2 platzieren**</span><span class="sxs-lookup"><span data-stu-id="c5563-156">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
