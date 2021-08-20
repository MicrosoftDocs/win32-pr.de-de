---
title: IMsTscAxEvents OnConnected-Methode
description: Wird aufgerufen, wenn das Clientsteuersystem eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost) herstellen wird.
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- OnConnected-Remotedesktopdienste
- OnConnected-Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnConnected-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9dfa60dee2c470e54c1900bc94aef5cdcb38835aa5e112f9ab5da0a9cce449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118853840"
---
# <a name="imstscaxeventsonconnected-method"></a>IMsTscAxEvents::OnConnected-Methode

Wird aufgerufen, wenn das Clientsteuersystem eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost) herstellen wird.

## <a name="syntax"></a>Syntax


```C++
void OnConnected();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Implementieren Sie diese Methode in der Ereignissenke, um eine Benachrichtigung zu erhalten, dass das Steuerelement eine Verbindung mit einem RD-Sitzungshost hergestellt hat.

Weitere Informationen zum Aufrufen dieser Methode finden Sie im [**IMsTscAxEvents::OnLoginComplete-Ereignis.**](imstscaxevents-onlogincomplete.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

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

 

 





