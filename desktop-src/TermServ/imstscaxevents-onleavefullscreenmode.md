---
title: IMsTscAxEvents OnLeaveFullScreenMode-Methode
description: Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die Tastenkombination im Vollbildmodus drückt (STRG+ALT+BREAK).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- OnLeaveFullScreenMode-Methode Remotedesktopdienste
- OnLeaveFullScreenMode-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnLeaveFullScreenMode-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efacca782d771337ffe3419bd9820be268cacc1ae6f7d33f04a4bb8127079c7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138443"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a>IMsTscAxEvents::OnLeaveFullScreenMode-Methode

Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die [Tastenkombination](terminal-services-shortcut-keys.md) im Vollbildmodus drückt (STRG+ALT+BREAK).

## <a name="syntax"></a>Syntax


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





