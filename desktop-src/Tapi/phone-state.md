---
description: TAPI sendet die Telefon \_ Zustands Meldung immer dann an eine Anwendung, wenn sich der Status eines Telefon Geräts ändert.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: PHONE_STATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367421"
---
# <a name="phone_state-message"></a><span data-ttu-id="c59fd-103">Telefon \_ Zustands Meldung</span><span class="sxs-lookup"><span data-stu-id="c59fd-103">PHONE\_STATE message</span></span>

<span data-ttu-id="c59fd-104">TAPI sendet die **Telefon \_ Zustands** Meldung immer dann an eine Anwendung, wenn sich der Status eines Telefon Geräts ändert.</span><span class="sxs-lookup"><span data-stu-id="c59fd-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c59fd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c59fd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c59fd-106">*hphone*</span><span class="sxs-lookup"><span data-stu-id="c59fd-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="c59fd-107">Ein Handle für das Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="c59fd-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="c59fd-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="c59fd-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c59fd-109">Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c59fd-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="c59fd-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c59fd-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c59fd-111">Der Telefon Zustand, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c59fd-111">The phone state that has changed.</span></span> <span data-ttu-id="c59fd-112">Dieser Parameter verwendet eine der [**phonestate- \_ Konstanten**](phonestate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c59fd-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59fd-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c59fd-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c59fd-114">Telefon Zustands abhängige Informationen, die die Statusänderung beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c59fd-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="c59fd-115">Dieser Parameter wird nicht verwendet, wenn mehrere Flags in *dwParam1* festgelegt sind, da sich mehrere Status Elemente geändert haben.</span><span class="sxs-lookup"><span data-stu-id="c59fd-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="c59fd-116">Die Anwendung sollte [**phonegetstatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) aufrufen, um einen kompletten Satz von Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c59fd-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="c59fd-117">Wenn *dwParam1* der phonestate- \_ Besitzer ist, enthält *dwParam2* die neue Anzahl von Besitzern.</span><span class="sxs-lookup"><span data-stu-id="c59fd-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="c59fd-118">Wenn *dwParam1* phonestate \_ Monitors ist, enthält *dwParam2* die neue Anzahl von Monitoren.</span><span class="sxs-lookup"><span data-stu-id="c59fd-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="c59fd-119">Wenn *dwParam1* "phonestate \_ Lamp" ist, enthält *dwParam2* den Schaltflächen-/Lamp-Bezeichner der geänderten Lamp.</span><span class="sxs-lookup"><span data-stu-id="c59fd-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="c59fd-120">Wenn *dwParam1* phonestate \_ ringmode ist, enthält *dwParam2* den neuen Ring Modus.</span><span class="sxs-lookup"><span data-stu-id="c59fd-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="c59fd-121">Wenn *dwParam1* phonestate \_ Handset, Speaker oder Headset ist, enthält *dwParam2* den neuen Modus "huokswitch" dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="c59fd-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="c59fd-122">Dieser Parameter verwendet eine der [**phonehuokswitchmode- \_ Konstanten**](phonehookswitchmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c59fd-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59fd-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c59fd-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c59fd-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c59fd-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c59fd-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c59fd-125">Return value</span></span>

<span data-ttu-id="c59fd-126">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="c59fd-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c59fd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59fd-127">Remarks</span></span>

<span data-ttu-id="c59fd-128">Das Senden der **Telefon \_ Zustands** Meldung an die Anwendung kann mithilfe von " [**phonesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) " und " [**phonegetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)" gesteuert und abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="c59fd-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="c59fd-129">Standardmäßig ist diese Meldung für alle Zustandsänderungen deaktiviert, mit Ausnahme von "phonestate \_ Reit", die nicht deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c59fd-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="c59fd-130">Diese Nachricht wird an alle Anwendungen gesendet, die über ein Handle für das Telefon verfügen, einschließlich derjenigen, die [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) aufgerufen haben, wobei der *dwprivileges* -Parameter auf phoneprivilege \_ Owner oder phoneprivilege Monitor festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="c59fd-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="c59fd-131">Eine **Telefon \_ Zustands** Meldung mit einer Anzeige von Besitzern und/oder Monitoren wird an Anwendungen gesendet, die bereits über ein Handle für das Telefon verfügen.</span><span class="sxs-lookup"><span data-stu-id="c59fd-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="c59fd-132">Dies kann das Ergebnis einer anderen Anwendung sein, die den Besitz oder die Überwachung des Telefon Geräts mit [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneclose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) oder [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)ändert.</span><span class="sxs-lookup"><span data-stu-id="c59fd-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="c59fd-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c59fd-133">Requirements</span></span>



| <span data-ttu-id="c59fd-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c59fd-134">Requirement</span></span> | <span data-ttu-id="c59fd-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c59fd-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c59fd-136">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c59fd-136">TAPI version</span></span><br/> | <span data-ttu-id="c59fd-137">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c59fd-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c59fd-138">Header</span><span class="sxs-lookup"><span data-stu-id="c59fd-138">Header</span></span><br/>       | <dl> <span data-ttu-id="c59fd-139"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59fd-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59fd-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c59fd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59fd-141">**Telefon \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="c59fd-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="c59fd-142">**Phonecaps**</span><span class="sxs-lookup"><span data-stu-id="c59fd-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="c59fd-143">**phoneclose**</span><span class="sxs-lookup"><span data-stu-id="c59fd-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="c59fd-144">**phonegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="c59fd-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="c59fd-145">**phonegetstatus**</span><span class="sxs-lookup"><span data-stu-id="c59fd-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="c59fd-146">**phonegetstatus Messages**</span><span class="sxs-lookup"><span data-stu-id="c59fd-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="c59fd-147">**phoneinitialize**</span><span class="sxs-lookup"><span data-stu-id="c59fd-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="c59fd-148">**phoneinitializeex**</span><span class="sxs-lookup"><span data-stu-id="c59fd-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="c59fd-149">**phoneopen**</span><span class="sxs-lookup"><span data-stu-id="c59fd-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="c59fd-150">**phonesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="c59fd-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="c59fd-151">**phoneshutdown**</span><span class="sxs-lookup"><span data-stu-id="c59fd-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




