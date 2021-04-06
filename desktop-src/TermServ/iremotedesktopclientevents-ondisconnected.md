---
title: Iremotedesktopclientevents-Methode (nicht getrennt)
description: Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Ongetrennte Methode Remotedesktopdienste
- Ongetrennte Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, ongetrennte-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742384"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>Iremotedesktopclientevents:: ongetrennte-Methode

Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde.

## <a name="syntax"></a>Syntax


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
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

 

 





