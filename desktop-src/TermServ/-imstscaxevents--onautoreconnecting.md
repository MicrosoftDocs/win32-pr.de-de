---
title: IMsTscAxEvents OnAutoReconnecting-Methode
description: Wird aufgerufen, wenn ein Client gerade eine Sitzung automatisch mit einem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) verbindet. | IMsTscAxEvents OnAutoReconnecting-Methode
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting-Methode Remotedesktopdienste
- OnAutoReconnecting-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnAutoReconnecting-Methode
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
ms.openlocfilehash: 2a26bb57416cd73f6d838ab08167923c4900b7b923a6a6f411239bbacd3fdbac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309140"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>IMsTscAxEvents::OnAutoReconnecting-Methode

Wird aufgerufen, wenn ein Client gerade eine Sitzung automatisch mit einem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) verbindet.

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

*disconnectReason* \[ In\]
</dt> <dd>

Code, der den Grund für die letzte Sitzungstrennung beschreibt.

</dd> <dt>

*attemptCount* \[ In\]
</dt> <dd>

Anzahl der Versuche, die im aktuellen prozess der automatischen Wiederherstellung der Verbindung unternommen wurden. Diese Anzahl erhöht sich für jeden unternommenen Versuch um eins.

</dd> <dt>

*pArcContinueStatus* \[ out\]
</dt> <dd>

Zeiger auf einen zurückgegebenen Code, der den Zustand des automatischen Verbindungswiederherstellungsprozesses angibt. Dieser Code kann zurückgesetzt werden, um den Status des aktuellen prozesses für die automatische Wiederherstellung der Verbindung zu ändern.

Weitere Informationen zum Zurücksetzen dieses Codes finden Sie im Abschnitt "Hinweise".

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic® (0)


</dt> <dd>

Der Prozess der erneuten Verbindung wird automatisch ausgeführt. Dies ist der Standardwert.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop® (1)


</dt> <dd>

Der Prozess zum Wiederherstellen der Verbindung wurde beendet.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual® (2)


</dt> <dd>

Der Prozess der erneuten Verbindung wird manuell ausgeführt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Implementieren Sie diese Methode in Ihrer Ereignissenke, um eine Benachrichtigung zu erhalten, dass das Steuerelement eine Verbindung mit einem RD-Sitzungshost Server wieder hersetzt.

Wenn der Zustand des automatischen Verbindungswiederherstellungsprozesses geändert wird, indem der Wert des *pArcContinueStatus-Parameters* auf **autoReconnectContinueAutomatic** festgelegt wird, funktioniert diese Methode in einem reinen Empfehlungsmodus. Container können auf dieses Ereignis auf Benachrichtigungen lauschen, dass der automatische Verbindungswiederherstellungsprozess fortgesetzt wird. Das Steuerelement versucht automatisch weiterhin, eine Verbindung basierend auf seiner eigenen internen Zeitsteuerung und Der Anzahl der Versuche herzustellen. Diese Methode wird bei jedem automatischen Erneutverbindungsversuch aufgerufen, um den Container zu benachrichtigen.

Wenn der Status des automatischen Verbindungswiederherstellungsprozesses durch Festlegen des Werts des *pArcContinueStatus-Parameters* auf **autoReconnectContinueStop** geändert wird, wird der aktuelle Versuch der automatischen Erneutverbindung beendet, eine Benachrichtigung zum Trennen der Verbindung wird an den Container gesendet, und es werden keine weiteren automatischen Benachrichtigungen zur erneuten Verbindung ausgegeben.

> [!Note]  
> Verwenden Sie die [**EnableAutoReconnect-Eigenschaft,**](imsrdpclientadvancedsettings2-enableautoreconnect.md) um die automatische wiederherzustellende Verbindung zu aktivieren oder zu deaktivieren.

 

Wenn der Status des automatischen Verbindungswiederherstellungsprozesses durch Festlegen des Werts des *pArcContinueStatus-Parameters* auf **autoReconnectContinueManual** geändert wird, steuert der Container den automatischen Erneutverbindungsprozess manuell, indem er Verbinden aufruft, um einen Verbindungsversuch auszulösen, oder [**Trennen,**](imstscax-disconnect.md) um den automatischen Verbindungswiederherstellungsprozess abzubrechen. [](imstscax-connect.md) Sobald dieses Steuerelement auf diesen Wert festgelegt ist, werden keine automatischen Verbindungsversuche mehr unternommen, und es wird zur Richtlinie des Containers, **Verbinden** Aufrufe zum Auslösen automatischer Erneutverbindungsversuche vorzunehmen. Dies geschieht, wenn der Container ein benutzerdefiniertes Benutzeroberflächenverhalten für die automatische wiederherzustellende Verbindung bereitstellt, z. B. das Neustarten einer gelöschten RAS- oder VPN-Verbindung vor dem automatischen Erneut herstellen.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





