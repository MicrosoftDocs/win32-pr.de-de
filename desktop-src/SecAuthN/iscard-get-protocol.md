---
description: Ruft den Bezeichner des zurzeit auf der Smartcard verwendeten Protokolls ab.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'Iscard:: get_Protocol-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348049"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="3734c-103">Iscard:: get- \_ Protokoll Methode</span><span class="sxs-lookup"><span data-stu-id="3734c-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="3734c-104">\[Die Methode " **get \_ Protocol** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3734c-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3734c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3734c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3734c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3734c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3734c-107">Die **get \_ Protocol** -Methode ruft den Bezeichner des Protokolls ab, das zurzeit auf der [*Smartcard*](../secgloss/s-gly.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3734c-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3734c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3734c-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="3734c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3734c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3734c-110">*pprotocol* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3734c-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3734c-111">Zeiger auf den Protokoll Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="3734c-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3734c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3734c-112">Return value</span></span>

<span data-ttu-id="3734c-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3734c-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3734c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3734c-114">Return code</span></span>                                                                                  | <span data-ttu-id="3734c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3734c-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="3734c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3734c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3734c-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3734c-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="3734c-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3734c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3734c-119">Der *pprotocol* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3734c-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="3734c-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3734c-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3734c-121">Ein fehlerhafter Zeiger wurde in " *pprotocol*" übergeben.</span><span class="sxs-lookup"><span data-stu-id="3734c-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3734c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3734c-122">Remarks</span></span>

<span data-ttu-id="3734c-123">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3734c-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3734c-124">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3734c-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3734c-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3734c-125">Examples</span></span>

<span data-ttu-id="3734c-126">Das folgende Beispiel zeigt, wie Sie den Bezeichner des Protokolls abrufen, das zurzeit auf der Smartcard verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3734c-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="3734c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3734c-127">Requirements</span></span>



| <span data-ttu-id="3734c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3734c-128">Requirement</span></span> | <span data-ttu-id="3734c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3734c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3734c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3734c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3734c-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3734c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3734c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3734c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3734c-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3734c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3734c-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3734c-134">End of client support</span></span><br/>    | <span data-ttu-id="3734c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3734c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3734c-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3734c-136">End of server support</span></span><br/>    | <span data-ttu-id="3734c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3734c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3734c-138">Header</span><span class="sxs-lookup"><span data-stu-id="3734c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3734c-139"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3734c-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="3734c-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3734c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="3734c-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3734c-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3734c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3734c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3734c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3734c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3734c-144">IID</span><span class="sxs-lookup"><span data-stu-id="3734c-144">IID</span></span><br/>                      | <span data-ttu-id="3734c-145">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="3734c-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3734c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3734c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3734c-147">**\_ATR erhalten**</span><span class="sxs-lookup"><span data-stu-id="3734c-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="3734c-148">**\_cardhandle erhalten**</span><span class="sxs-lookup"><span data-stu-id="3734c-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="3734c-149">**\_Kontext erhalten**</span><span class="sxs-lookup"><span data-stu-id="3734c-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="3734c-150">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="3734c-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="3734c-151">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="3734c-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
