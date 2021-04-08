---
title: Imstscaxevents (onconnected-Methode)
description: Wird aufgerufen, wenn das Client Steuerelement gerade eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server herstellt.
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der onconnected-Methode
- Onconnected-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onconnected-Methode
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
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741321"
---
# <a name="imstscaxeventsonconnected-method"></a>Imstscaxevents:: onconnected-Methode

Wird aufgerufen, wenn das Client Steuerelement gerade eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server herstellt.

## <a name="syntax"></a>Syntax


```C++
void OnConnected();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um eine Benachrichtigung zu erhalten, dass das Steuerelement eine Verbindung mit einem RD-Sitzungshost Server hergestellt hat.

Weitere Informationen zum Aufrufen dieser Methode finden Sie im [**imstscaxevents:: onlogincomplete**](imstscaxevents-onlogincomplete.md) -Ereignis.

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

 

 





