---
title: IMsTscAxEvents OnIdleTimeoutNotification-Methode
description: Wird aufgerufen, wenn der Benutzer während des von der IMsRdpClientAdvancedSettings-Methode festgelegten Zeitraums keine Maus- oder Tastatureingaben erhalten \_ hat.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- OnIdleTimeoutNotification-Remotedesktopdienste
- OnIdleTimeoutNotification-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnIdleTimeoutNotification-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356414d03a6b102f37f93205e0dbb8c3261cffbbb5b71a58cdb3f80acda09212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125120"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>IMsTscAxEvents::OnIdleTimeoutNotification-Methode

Wird aufgerufen, wenn der Benutzer während des von der [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout-Methode**](imsrdpclientadvancedsettings-minutestoidletimeout.md) festgelegten Zeitraums keine Maus- oder Tastatureingaben erhalten hat.

## <a name="syntax"></a>Syntax


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Standardmäßig ist der Wert der [**MinutesToIdleTimeout-Eigenschaft**](imsrdpclientadvancedsettings-minutestoidletimeout.md) auf 0 (null) festgelegt, und das System überwacht keine Leerlauftimeouts. Dieses Ereignis tritt nur auf, wenn die -Eigenschaft auf einen Wert ungleich 0 (null) festgelegt ist.

Der Wert [**von MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) wird bei jedem Auftreten des Ereignisses automatisch zurückgesetzt.

Anwendungen können [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in Situationen verwenden, in denen es sinnvoll ist, die Verbindung eines Benutzers zu trennen. z. B. in einem Kiosk oder einem anderen öffentlichen Terminalszenario.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





