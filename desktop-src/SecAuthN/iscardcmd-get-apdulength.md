---
description: Bestimmt die Länge (in Byte) der Anwendungsprotokoll-Dateneinheit (APDU).
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'Iscardcmd:: get_ApduLength-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1535d2b4b67861b42719506ebd48cca4c49d5c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760116"
---
# <a name="iscardcmdget_apdulength-method"></a><span data-ttu-id="6f455-103">Iscardcmd:: get \_ apdulength-Methode</span><span class="sxs-lookup"><span data-stu-id="6f455-103">ISCardCmd::get\_ApduLength method</span></span>

<span data-ttu-id="6f455-104">\[Die Methode " **get \_ apdulength** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6f455-104">\[The **get\_ApduLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6f455-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f455-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6f455-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6f455-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6f455-107">Die **get \_ apdulength** -Methode bestimmt die Länge (in Byte) der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="6f455-107">The **get\_ApduLength** method determines the length, in bytes, f the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f455-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f455-108">Syntax</span></span>


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="6f455-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f455-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f455-110">*plsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f455-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f455-111">Zeiger auf die Länge von APDU.</span><span class="sxs-lookup"><span data-stu-id="6f455-111">Pointer to the length of the APDU.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f455-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f455-112">Return value</span></span>

<span data-ttu-id="6f455-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6f455-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6f455-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6f455-114">Return code</span></span>                                                                                   | <span data-ttu-id="6f455-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f455-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6f455-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6f455-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6f455-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="6f455-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6f455-119">Der *plsize* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6f455-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="6f455-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6f455-121">Es wurde ein fehlerhafter Zeiger an *plsize* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6f455-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="6f455-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6f455-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6f455-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="6f455-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f455-124">Remarks</span></span>

<span data-ttu-id="6f455-125">Rufen Sie zum Abrufen der RAW [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) aus dem Byte Puffer, der über einen **IStream** zugeordnet ist, der die APDU-Nachricht enthält, [**get \_ APDU**](iscardcmd-get-apdu.md)auf.</span><span class="sxs-lookup"><span data-stu-id="6f455-125">To retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="6f455-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="6f455-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="6f455-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6f455-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6f455-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6f455-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6f455-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f455-129">Examples</span></span>

<span data-ttu-id="6f455-130">Im folgenden Beispiel wird gezeigt, wie die APDU-Länge ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6f455-130">The following example shows how to retrieve the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) length.</span></span> <span data-ttu-id="6f455-131">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="6f455-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="6f455-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f455-132">Requirements</span></span>



| <span data-ttu-id="6f455-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f455-133">Requirement</span></span> | <span data-ttu-id="6f455-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6f455-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f455-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f455-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6f455-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f455-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6f455-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f455-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6f455-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f455-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f455-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6f455-139">End of client support</span></span><br/>    | <span data-ttu-id="6f455-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f455-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6f455-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6f455-141">End of server support</span></span><br/>    | <span data-ttu-id="6f455-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f455-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6f455-143">Header</span><span class="sxs-lookup"><span data-stu-id="6f455-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f455-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f455-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6f455-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f455-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f455-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6f455-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f455-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f455-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f455-149">IID</span><span class="sxs-lookup"><span data-stu-id="6f455-149">IID</span></span><br/>                      | <span data-ttu-id="6f455-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="6f455-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6f455-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f455-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f455-152">**\_APDU erhalten**</span><span class="sxs-lookup"><span data-stu-id="6f455-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="6f455-153">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="6f455-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
