---
title: IRemoteDesktopClientEvents OnDisconnected-Methode
description: Wird aufgerufen, wenn das Clientsteuerelement von einer Remotesitzung getrennt wurde.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- OnDisconnected-Methode Remotedesktopdienste
- OnDisconnected-Methode Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnDisconnected-Methode
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
ms.openlocfilehash: 5e93ebf7c85e4015539cbbcc15723cdfed9c7d181741925c1a97c93ccc4326eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124900"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>IRemoteDesktopClientEvents::OnDisconnected-Methode

Wird aufgerufen, wenn das Clientsteuerelement von einer Remotesitzung getrennt wurde.

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

 

 





