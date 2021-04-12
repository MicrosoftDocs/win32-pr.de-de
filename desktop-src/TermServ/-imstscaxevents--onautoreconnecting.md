---
title: Imstscaxevents onautoreconnecting-Methode
description: Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet. | Imstscaxevents onautoreconnecting-Methode
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Onautoreconnecting-Methode Remotedesktopdienste
- Onautoreconnecting-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onautoreconnecting-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353488"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="9ce90-107">Imstscaxevents:: onautoreconnecting-Methode</span><span class="sxs-lookup"><span data-stu-id="9ce90-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="9ce90-108">Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet.</span><span class="sxs-lookup"><span data-stu-id="9ce90-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce90-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ce90-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="9ce90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ce90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce90-111">*disconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ce90-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce90-112">Code, der den Grund für das Trennen der letzten Sitzung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9ce90-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="9ce90-113">*Anzahl* \[ der Versuche in\]</span><span class="sxs-lookup"><span data-stu-id="9ce90-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce90-114">Anzahl der Versuche, die im aktuellen automatischen erneuten Verbindungsvorgang durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="9ce90-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="9ce90-115">Diese Anzahl wird für jeden erfolgten Versuch um eins erhöht.</span><span class="sxs-lookup"><span data-stu-id="9ce90-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="9ce90-116">*parameestatusstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9ce90-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce90-117">Ein Zeiger auf einen zurückgegebenen Code, der den Zustand des automatischen erneuten Verbindungs Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="9ce90-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="9ce90-118">Dieser Code kann zurückgesetzt werden, um den Status des aktuellen automatischen erneuten Verbindungs Vorgangs zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9ce90-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="9ce90-119">Weitere Informationen zum Zurücksetzen dieses Codes finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="9ce90-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="9ce90-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoreconnectcontinueautomatic \* \* \* \* (0)</span><span class="sxs-lookup"><span data-stu-id="9ce90-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="9ce90-121">Der Vorgang zur erneuten Verbindungs Herstellung wird automatisch durchgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9ce90-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="9ce90-122">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9ce90-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="9ce90-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoreconnectcontinuestop \* \* \* \* (1)</span><span class="sxs-lookup"><span data-stu-id="9ce90-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ce90-124">Der Vorgang zum erneuten Herstellen der Verbindung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="9ce90-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="9ce90-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoreconnectcontinuemanual \* \* \* \* (2)</span><span class="sxs-lookup"><span data-stu-id="9ce90-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="9ce90-126">Der Vorgang zur erneuten Verbindungs Herstellung erfolgt manuell.</span><span class="sxs-lookup"><span data-stu-id="9ce90-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce90-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ce90-127">Return value</span></span>

<span data-ttu-id="9ce90-128">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9ce90-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ce90-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ce90-129">Remarks</span></span>

<span data-ttu-id="9ce90-130">Implementieren Sie diese Methode in der Ereignis Senke, um eine Benachrichtigung zu erhalten, dass das Steuerelement eine Verbindung mit einem RD-Sitzungshost Server wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="9ce90-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="9ce90-131">Wenn der Status des automatischen erneuten Verbindungs Vorgangs geändert wird, *indem der Wert des Parameters "* Parameter Parameter" auf " **autoreconnectcontinueautomatic**" festgelegt wird, funktioniert diese Methode in einem reinen Beratungsmodus.</span><span class="sxs-lookup"><span data-stu-id="9ce90-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="9ce90-132">Container können dieses Ereignis auf Benachrichtigungen überwachen, die den automatischen erneuten Verbindungsvorgang fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="9ce90-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="9ce90-133">Das-Steuerelement versucht automatisch, eine Verbindung basierend auf der eigenen internen Zeitüberschreitung und der Anzahl der Versuche wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9ce90-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="9ce90-134">Diese Methode wird bei jedem automatischen erneuten Verbindungsversuch aufgerufen, um den Container zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="9ce90-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="9ce90-135">Wenn der Status des automatischen erneuten Verbindungs Vorgangs durch Festlegen des *Werts des Parameters "* Parameter" auf " **autoreconnectcontinuestop**" geändert wird, wird der aktuelle Versuch zur automatischen erneuten Verbindung beendet, eine Disconnect-Benachrichtigung wird an den Container gesendet, und es werden keine weiteren automatischen Verbindungs Benachrichtigungen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ce90-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="9ce90-136">Verwenden Sie die [**enableautoreconnetct**](imsrdpclientadvancedsettings2-enableautoreconnect.md) -Eigenschaft, um die automatische erneute Verbindungs Herstellung zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9ce90-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="9ce90-137">Wenn der Status des automatischen erneuten Verbindungs Vorgangs geändert wird, indem der *Wert des Parameters "* Parameter Parameter" auf " **autoreconnectcontinuemanual**" festgelegt wird, steuert der Container manuell den automatischen Vorgang zum erneuten Verbinden durch Aufrufen von [**Connect**](imstscax-connect.md) , um einen Verbindungsversuch zu initiieren oder die Verbindung zu [**trennen**](imstscax-disconnect.md) , um den automatischen Vorgang zum erneuten Herstellen der Verbindung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="9ce90-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="9ce90-138">Sobald dieser Wert festgelegt ist, beendet das Steuerelement keine automatischen Verbindungsversuche und wird zur Richtlinie des Containers, um **Verbindungs** Aufrufe durchführen, um automatische erneute Verbindungsversuche zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="9ce90-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="9ce90-139">Dies geschieht, wenn der Container das angepasste Verhalten der Benutzeroberfläche für die automatische erneute Verbindung bereitstellt, z. b. das Neustarten einer gelöschten RAS-oder VPN-Verbindung vor dem automatischen erneuten Verbindungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="9ce90-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="9ce90-140">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9ce90-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce90-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ce90-141">Requirements</span></span>



| <span data-ttu-id="9ce90-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ce90-142">Requirement</span></span> | <span data-ttu-id="9ce90-143">Wert</span><span class="sxs-lookup"><span data-stu-id="9ce90-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce90-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ce90-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce90-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ce90-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9ce90-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ce90-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce90-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ce90-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9ce90-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9ce90-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ce90-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ce90-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ce90-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9ce90-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ce90-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ce90-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce90-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ce90-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce90-153">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="9ce90-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





