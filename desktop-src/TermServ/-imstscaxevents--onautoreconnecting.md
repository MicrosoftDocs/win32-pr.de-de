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
# <a name="imstscaxeventsonautoreconnecting-method"></a>Imstscaxevents:: onautoreconnecting-Methode

Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet.

## <a name="syntax"></a>Syntax


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*disconnecverrat* \[ in\]
</dt> <dd>

Code, der den Grund für das Trennen der letzten Sitzung beschreibt.

</dd> <dt>

*Anzahl* \[ der Versuche in\]
</dt> <dd>

Anzahl der Versuche, die im aktuellen automatischen erneuten Verbindungsvorgang durchgeführt wurden. Diese Anzahl wird für jeden erfolgten Versuch um eins erhöht.

</dd> <dt>

*parameestatusstatus* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen zurückgegebenen Code, der den Zustand des automatischen erneuten Verbindungs Vorgangs angibt. Dieser Code kann zurückgesetzt werden, um den Status des aktuellen automatischen erneuten Verbindungs Vorgangs zu ändern.

Weitere Informationen zum Zurücksetzen dieses Codes finden Sie im Abschnitt "Hinweise".

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoreconnectcontinueautomatic * * * * (0)


</dt> <dd>

Der Vorgang zur erneuten Verbindungs Herstellung wird automatisch durchgesetzt. Dies ist der Standardwert.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoreconnectcontinuestop * * * * (1)


</dt> <dd>

Der Vorgang zum erneuten Herstellen der Verbindung wurde beendet.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoreconnectcontinuemanual * * * * (2)


</dt> <dd>

Der Vorgang zur erneuten Verbindungs Herstellung erfolgt manuell.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um eine Benachrichtigung zu erhalten, dass das Steuerelement eine Verbindung mit einem RD-Sitzungshost Server wiederherstellt.

Wenn der Status des automatischen erneuten Verbindungs Vorgangs geändert wird, *indem der Wert des Parameters "* Parameter Parameter" auf " **autoreconnectcontinueautomatic**" festgelegt wird, funktioniert diese Methode in einem reinen Beratungsmodus. Container können dieses Ereignis auf Benachrichtigungen überwachen, die den automatischen erneuten Verbindungsvorgang fortsetzen. Das-Steuerelement versucht automatisch, eine Verbindung basierend auf der eigenen internen Zeitüberschreitung und der Anzahl der Versuche wiederherzustellen. Diese Methode wird bei jedem automatischen erneuten Verbindungsversuch aufgerufen, um den Container zu benachrichtigen.

Wenn der Status des automatischen erneuten Verbindungs Vorgangs durch Festlegen des *Werts des Parameters "* Parameter" auf " **autoreconnectcontinuestop**" geändert wird, wird der aktuelle Versuch zur automatischen erneuten Verbindung beendet, eine Disconnect-Benachrichtigung wird an den Container gesendet, und es werden keine weiteren automatischen Verbindungs Benachrichtigungen ausgegeben.

> [!Note]  
> Verwenden Sie die [**enableautoreconnetct**](imsrdpclientadvancedsettings2-enableautoreconnect.md) -Eigenschaft, um die automatische erneute Verbindungs Herstellung zu aktivieren oder zu deaktivieren.

 

Wenn der Status des automatischen erneuten Verbindungs Vorgangs geändert wird, indem der *Wert des Parameters "* Parameter Parameter" auf " **autoreconnectcontinuemanual**" festgelegt wird, steuert der Container manuell den automatischen Vorgang zum erneuten Verbinden durch Aufrufen von [**Connect**](imstscax-connect.md) , um einen Verbindungsversuch zu initiieren oder die Verbindung zu [**trennen**](imstscax-disconnect.md) , um den automatischen Vorgang zum erneuten Herstellen der Verbindung abzubrechen. Sobald dieser Wert festgelegt ist, beendet das Steuerelement keine automatischen Verbindungsversuche und wird zur Richtlinie des Containers, um **Verbindungs** Aufrufe durchführen, um automatische erneute Verbindungsversuche zu initiieren. Dies geschieht, wenn der Container das angepasste Verhalten der Benutzeroberfläche für die automatische erneute Verbindung bereitstellt, z. b. das Neustarten einer gelöschten RAS-oder VPN-Verbindung vor dem automatischen erneuten Verbindungsvorgang.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





