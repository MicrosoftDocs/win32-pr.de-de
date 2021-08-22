---
title: IRemoteDesktopClientEvents OnAutoReconnecting-Methode
description: Wird aufgerufen, wenn das Clientsteuersystem versucht, eine Verbindung mit einer Remotesitzung automatisch wiederhergestellt zu haben.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting-Remotedesktopdienste
- OnAutoReconnecting-Methode Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnAutoReconnecting-Methode
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
ms.openlocfilehash: 7246b8822b3d3abed5d483f52c64eee88d67f99694bda44c5d8f72318cb2c04a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511730"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>IRemoteDesktopClientEvents::OnAutoReconnecting-Methode

Wird aufgerufen, wenn das Clientsteuersystem versucht, eine Verbindung mit einer Remotesitzung automatisch wiederhergestellt zu haben.

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

*disconnectReason* \[ In\]
</dt> <dd>

Der Grund für das Disconnect-Ereignis.

</dd> <dt>

*ExtendedDisconnectReason* \[ In\]
</dt> <dd>

Erweiterte Informationen für das Disconnect-Ereignis.

</dd> <dt>

*disconnectErrorMessage* \[ In\]
</dt> <dd>

Die Fehlermeldung für das Disconnect-Ereignis.

</dd> <dt>

*networkAvailable* \[ In\]
</dt> <dd>

Gibt an, ob das Netzwerk verfügbar ist.

</dd> <dt>

*attemptCount* \[ In\]
</dt> <dd>

Versuchen Sie, dies zu versuchen.

</dd> <dt>

*maxAttemptCount* \[ In\]
</dt> <dd>

Die maximale Anzahl von Verbindungsversuchen wird ausgeführt.

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
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





