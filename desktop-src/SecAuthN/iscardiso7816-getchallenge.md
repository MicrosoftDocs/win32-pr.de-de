---
description: Die getchallenge-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der eine Herausforderung (z. b. eine Zufallszahl) für die Verwendung in einer sicherheitsbezogenen Prozedur ausgibt.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: 'ISCardISO7816:: getchallenge-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042698"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="48e83-103">ISCardISO7816:: getchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="48e83-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="48e83-104">\[Die **getchallenge** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="48e83-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="48e83-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48e83-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="48e83-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="48e83-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="48e83-107">Die **getchallenge** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der eine Herausforderung (z. b. eine Zufallszahl) für die Verwendung in einer sicherheitsbezogenen Prozedur ausgibt.</span><span class="sxs-lookup"><span data-stu-id="48e83-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e83-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e83-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="48e83-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="48e83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e83-110">*lbyteserwartet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48e83-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e83-111">Maximale Länge der erwarteten Antwort.</span><span class="sxs-lookup"><span data-stu-id="48e83-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="48e83-112">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="48e83-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48e83-113">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="48e83-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="48e83-114">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="48e83-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="48e83-115">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48e83-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e83-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48e83-116">Return value</span></span>

<span data-ttu-id="48e83-117">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="48e83-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="48e83-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="48e83-118">Return code</span></span>                                                                                   | <span data-ttu-id="48e83-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e83-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="48e83-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="48e83-121">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="48e83-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="48e83-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="48e83-123">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="48e83-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="48e83-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="48e83-125">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="48e83-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="48e83-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="48e83-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="48e83-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="48e83-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48e83-128">Remarks</span></span>

<span data-ttu-id="48e83-129">Die Herausforderung ist zumindest für den nächsten Befehl gültig.</span><span class="sxs-lookup"><span data-stu-id="48e83-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="48e83-130">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="48e83-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="48e83-131">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="48e83-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="48e83-132">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="48e83-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48e83-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48e83-133">Requirements</span></span>



| <span data-ttu-id="48e83-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48e83-134">Requirement</span></span> | <span data-ttu-id="48e83-135">Wert</span><span class="sxs-lookup"><span data-stu-id="48e83-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e83-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48e83-136">Minimum supported client</span></span><br/> | <span data-ttu-id="48e83-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48e83-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48e83-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48e83-138">Minimum supported server</span></span><br/> | <span data-ttu-id="48e83-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48e83-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48e83-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="48e83-140">End of client support</span></span><br/>    | <span data-ttu-id="48e83-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48e83-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="48e83-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="48e83-142">End of server support</span></span><br/>    | <span data-ttu-id="48e83-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48e83-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="48e83-144">Header</span><span class="sxs-lookup"><span data-stu-id="48e83-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="48e83-145"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48e83-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="48e83-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="48e83-147"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48e83-148">DLL</span><span class="sxs-lookup"><span data-stu-id="48e83-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e83-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e83-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48e83-150">IID</span><span class="sxs-lookup"><span data-stu-id="48e83-150">IID</span></span><br/>                      | <span data-ttu-id="48e83-151">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="48e83-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="48e83-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48e83-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e83-153">**Externalauthenticate**</span><span class="sxs-lookup"><span data-stu-id="48e83-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="48e83-154">**Internalauthenticate**</span><span class="sxs-lookup"><span data-stu-id="48e83-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="48e83-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="48e83-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
