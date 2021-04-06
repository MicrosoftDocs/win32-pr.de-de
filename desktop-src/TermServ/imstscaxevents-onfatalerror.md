---
title: Imstscaxevents onfatalerror-Methode
description: Wird aufgerufen, wenn das Client Steuerelement einen schwerwiegenden Fehler feststellt.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Onfatalerror-Methode Remotedesktopdienste
- Onfatalerror-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onfatalerror-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859032"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="42a00-106">Imstscaxevents:: onfatalerror-Methode</span><span class="sxs-lookup"><span data-stu-id="42a00-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="42a00-107">Wird aufgerufen, wenn das Client Steuerelement einen schwerwiegenden Fehler feststellt.</span><span class="sxs-lookup"><span data-stu-id="42a00-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a00-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a00-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="42a00-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="42a00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a00-110">*errorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a00-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a00-111">Gibt den Fehlercode an.</span><span class="sxs-lookup"><span data-stu-id="42a00-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="42a00-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="42a00-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-113">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="42a00-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="42a00-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="42a00-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-115">Interner Fehlercode 1.</span><span class="sxs-lookup"><span data-stu-id="42a00-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="42a00-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="42a00-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-117">Fehler aufgrund von nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="42a00-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="42a00-118"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="42a00-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-119">Ein Fenster Erstellungs Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="42a00-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="42a00-120"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="42a00-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-121">Interner Fehlercode 2.</span><span class="sxs-lookup"><span data-stu-id="42a00-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="42a00-122"><span id="5"></span>**5@@**</span><span class="sxs-lookup"><span data-stu-id="42a00-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-123">Interner Fehlercode 3.</span><span class="sxs-lookup"><span data-stu-id="42a00-123">Internal error code 3.</span></span> <span data-ttu-id="42a00-124">Dies ist kein gültiger Status.</span><span class="sxs-lookup"><span data-stu-id="42a00-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="42a00-125"><span id="6"></span>**6**</span><span class="sxs-lookup"><span data-stu-id="42a00-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-126">Interner Fehlercode 4.</span><span class="sxs-lookup"><span data-stu-id="42a00-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="42a00-127"><span id="7"></span>**19.00**</span><span class="sxs-lookup"><span data-stu-id="42a00-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-128">Nicht BEHEB barer Fehler während der Client Verbindung.</span><span class="sxs-lookup"><span data-stu-id="42a00-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="42a00-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="42a00-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="42a00-130">Winsock-Initialisierungsfehler.</span><span class="sxs-lookup"><span data-stu-id="42a00-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a00-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42a00-131">Return value</span></span>

<span data-ttu-id="42a00-132">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="42a00-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a00-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a00-133">Remarks</span></span>

<span data-ttu-id="42a00-134">Als Reaktion auf dieses Ereignis zeigt der Container eine Fehlermeldung an und wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="42a00-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="42a00-135">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="42a00-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42a00-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42a00-136">Requirements</span></span>



| <span data-ttu-id="42a00-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a00-137">Requirement</span></span> | <span data-ttu-id="42a00-138">Wert</span><span class="sxs-lookup"><span data-stu-id="42a00-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42a00-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42a00-139">Minimum supported client</span></span><br/> | <span data-ttu-id="42a00-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42a00-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="42a00-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42a00-141">Minimum supported server</span></span><br/> | <span data-ttu-id="42a00-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42a00-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="42a00-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="42a00-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="42a00-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a00-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="42a00-145">DLL</span><span class="sxs-lookup"><span data-stu-id="42a00-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a00-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a00-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="42a00-147">IID</span><span class="sxs-lookup"><span data-stu-id="42a00-147">IID</span></span><br/>                      | <span data-ttu-id="42a00-148">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="42a00-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="42a00-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42a00-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a00-150">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="42a00-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





