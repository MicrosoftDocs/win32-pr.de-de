---
title: Iremotedesktopclientevents onautoreconnecting-Methode
description: Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Onautoreconnecting-Methode Remotedesktopdienste
- Onautoreconnecting-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onautoreconnecting-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519007"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>Iremotedesktopclientevents:: onautoreconnecting-Methode

Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen.

## <a name="syntax"></a>Syntax


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*disconnecverrat* \[ in\]
</dt> <dd>

Der Grund für das Trennungs Ereignis.

</dd> <dt>

*Extendeddisconnecverrat* \[ in\]
</dt> <dd>

Erweiterte Informationen für das Disconnect-Ereignis.

</dd> <dt>

*disconnecterrormessage* \[ in\]
</dt> <dd>

Die Fehlermeldung für das Disconnect-Ereignis.

</dd> <dt>

*NetworkAvailable* \[ in\]
</dt> <dd>

Gibt an, ob das Netzwerk verfügbar ist.

</dd> <dt>

*Anzahl* \[ der Versuche in\]
</dt> <dd>

Der Versuch, dies zu tun.

</dd> <dt>

*maxder-Anzahl* \[ in\]
</dt> <dd>

Die maximale Anzahl von Wiederholungs versuchen für die Verbindung wird ausgeführt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclientevents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





