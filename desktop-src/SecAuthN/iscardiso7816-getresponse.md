---
description: Die GetResponse-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der APDU-Befehle (oder einen Teil eines APDU-Befehls) überträgt, die andernfalls nicht von den verfügbaren Protokollen übertragen werden konnten.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'ISCardISO7816:: GetResponse-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352426"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="6a9e0-103">ISCardISO7816:: GetResponse-Methode</span><span class="sxs-lookup"><span data-stu-id="6a9e0-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="6a9e0-104">\[Die **GetResponse** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6a9e0-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a9e0-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6a9e0-107">Die **GetResponse** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der APDU-Befehle (oder einen Teil eines APDU-Befehls) überträgt, die andernfalls nicht von den verfügbaren Protokollen übertragen werden konnten.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a9e0-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6a9e0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a9e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9e0-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9e0-111">Gemäß ISO 7816-4 sollte P1 gleich NULL (RFU) sein.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="6a9e0-112">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9e0-113">Gemäß ISO 7816-4 sollte P2 NULL (RFU) sein.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="6a9e0-114">*ldatalength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9e0-115">Länge der übertragenen Daten.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="6a9e0-116">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9e0-117">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="6a9e0-118">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="6a9e0-119">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a9e0-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a9e0-120">Return value</span></span>

<span data-ttu-id="6a9e0-121">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6a9e0-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6a9e0-122">Return code</span></span>                                                                                   | <span data-ttu-id="6a9e0-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a9e0-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6a9e0-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6a9e0-125">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6a9e0-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6a9e0-127">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6a9e0-128"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6a9e0-129">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6a9e0-130"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6a9e0-131">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6a9e0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a9e0-132">Remarks</span></span>

<span data-ttu-id="6a9e0-133">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="6a9e0-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="6a9e0-134">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6a9e0-135">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6a9e0-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9e0-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a9e0-136">Requirements</span></span>



| <span data-ttu-id="6a9e0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a9e0-137">Requirement</span></span> | <span data-ttu-id="6a9e0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="6a9e0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9e0-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a9e0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9e0-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6a9e0-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a9e0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9e0-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a9e0-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a9e0-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6a9e0-143">End of client support</span></span><br/>    | <span data-ttu-id="6a9e0-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a9e0-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6a9e0-145">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6a9e0-145">End of server support</span></span><br/>    | <span data-ttu-id="6a9e0-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a9e0-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6a9e0-147">Header</span><span class="sxs-lookup"><span data-stu-id="6a9e0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a9e0-148"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a9e0-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6a9e0-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a9e0-150"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a9e0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6a9e0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a9e0-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e0-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a9e0-153">IID</span><span class="sxs-lookup"><span data-stu-id="6a9e0-153">IID</span></span><br/>                      | <span data-ttu-id="6a9e0-154">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="6a9e0-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6a9e0-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a9e0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9e0-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6a9e0-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
