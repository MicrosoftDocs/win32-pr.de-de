---
title: IMsTscAxEvents OnEnterFullScreenMode-Methode
description: Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die Tastenkombination im Vollbildmodus drückt (STRG+ALT+BREAK).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- OnEnterFullScreenMode-Methode Remotedesktopdienste
- OnEnterFullScreenMode-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnEnterFullScreenMode-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e40da93f0e29fb183cea540b0f195d61c4969d65c2b7829bf86d8e3c8eba81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512400"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a>IMsTscAxEvents::OnEnterFullScreenMode-Methode

Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die [Tastenkombination](terminal-services-shortcut-keys.md) im Vollbildmodus drückt (STRG+ALT+BREAK).

## <a name="syntax"></a>Syntax


```C++
void OnEnterFullScreenMode();
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





