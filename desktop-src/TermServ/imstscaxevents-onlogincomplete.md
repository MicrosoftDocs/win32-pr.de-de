---
title: IMsTscAxEvents OnLoginComplete-Methode
description: Wird aufgerufen, wenn sich das Clientsteuerfeld erfolgreich bei einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) angemeldet hat. Dies wird im Windows Dialogfeld Anmeldung angezeigt.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- OnLoginComplete-Remotedesktopdienste
- OnLoginComplete-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnLoginComplete-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c89b494a250652e054e245eb0de3267a860bec1a193c7dc953f93fd0800c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138433"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>IMsTscAxEvents::OnLoginComplete-Methode

Wird aufgerufen, wenn sich das Clientsteuerfeld erfolgreich bei einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) angemeldet hat. Dies wird im Windows Dialogfeld Anmeldung angezeigt.

## <a name="syntax"></a>Syntax


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Implementieren Sie diese Methode in der Ereignissenke, um eine Benachrichtigung zu erhalten, dass die Anmeldung des Steuerelements abgeschlossen wurde.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie dieses Ereignis mithilfe von Skriptcode Visual Basic behandelt wird. In diesem Beispiel wird davon ausgegangen, dass Ihr Steuerelementobjekt "MsRdpClient" heißt.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



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

 

 





