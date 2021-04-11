---
description: Ruft den aktuellen Zustand der Smartcard ab.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: 'Iscard:: get_Status-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218512"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="c7054-103">Iscard:: get- \_ Status Methode</span><span class="sxs-lookup"><span data-stu-id="c7054-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="c7054-104">\[Die Methode " **get \_ Status** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c7054-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7054-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7054-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c7054-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c7054-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c7054-107">Die **get \_ Status** -Methode ruft den aktuellen [*Zustand*](../secgloss/s-gly.md) der [*Smartcard*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="c7054-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7054-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7054-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c7054-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7054-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7054-110">*pstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7054-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7054-111">Zeiger auf die Zustands Variable.</span><span class="sxs-lookup"><span data-stu-id="c7054-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7054-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7054-112">Return value</span></span>

<span data-ttu-id="c7054-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c7054-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c7054-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c7054-114">Return code</span></span>                                                                                  | <span data-ttu-id="c7054-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7054-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="c7054-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7054-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c7054-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c7054-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="c7054-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c7054-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c7054-119">Der *pstatus* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7054-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c7054-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c7054-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="c7054-121">Ein fehlerhafter Zeiger wurde in *pstatus* übergeben.</span><span class="sxs-lookup"><span data-stu-id="c7054-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7054-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7054-122">Remarks</span></span>

<span data-ttu-id="c7054-123">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c7054-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c7054-124">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c7054-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c7054-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7054-125">Examples</span></span>

<span data-ttu-id="c7054-126">Das folgende Beispiel zeigt das Abrufen des aktuellen Status der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="c7054-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="c7054-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7054-127">Requirements</span></span>



| <span data-ttu-id="c7054-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7054-128">Requirement</span></span> | <span data-ttu-id="c7054-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c7054-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7054-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7054-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7054-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7054-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c7054-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7054-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7054-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7054-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7054-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c7054-134">End of client support</span></span><br/>    | <span data-ttu-id="c7054-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7054-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c7054-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c7054-136">End of server support</span></span><br/>    | <span data-ttu-id="c7054-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7054-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c7054-138">Header</span><span class="sxs-lookup"><span data-stu-id="c7054-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7054-139"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c7054-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7054-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c7054-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7054-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7054-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7054-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c7054-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7054-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7054-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7054-144">IID</span><span class="sxs-lookup"><span data-stu-id="c7054-144">IID</span></span><br/>                      | <span data-ttu-id="c7054-145">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="c7054-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c7054-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7054-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7054-147">**\_ATR erhalten**</span><span class="sxs-lookup"><span data-stu-id="c7054-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="c7054-148">**\_cardhandle erhalten**</span><span class="sxs-lookup"><span data-stu-id="c7054-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="c7054-149">**\_Kontext erhalten**</span><span class="sxs-lookup"><span data-stu-id="c7054-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="c7054-150">**get- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="c7054-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="c7054-151">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="c7054-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
