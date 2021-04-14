---
title: Imstscaxevents onconnecting-Methode
description: Wird aufgerufen, wenn das Client Steuerelement mit dem Herstellen einer Verbindung mit einem Server als Reaktion auf einen Aufruf von imstscax Connect beginnt.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Onconnecting-Methode Remotedesktopdienste
- Onconnecting-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onconnecting-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391520"
---
# <a name="imstscaxeventsonconnecting-method"></a>Imstscaxevents:: onconnecting-Methode

Wird aufgerufen, wenn das Client Steuerelement mit dem Herstellen einer Verbindung mit einem Server als Reaktion auf einen Aufruf von [**imstscax:: Connect**](imstscax-connect.md)beginnt.

## <a name="syntax"></a>Syntax


```C++
void OnConnecting();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass das Steuerelement mit dem verbinden begonnen

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie dieses Ereignis mit Visual Basic Skriptcode behandelt wird. In diesem Beispiel wird davon ausgegangen, dass das Steuerelement Objekt den Namen "MsRdpClient" hat.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



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

 

 





