---
title: Imstscaxevents onenterfullscreenmode-Methode
description: Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Onenterfullscreenmode-Methode Remotedesktopdienste
- Onenterfullscreenmode-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onenterfullscreenmode-Methode
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
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956668"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a>Imstscaxevents:: onenterfullscreenmode-Methode

Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).

## <a name="syntax"></a>Syntax


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





