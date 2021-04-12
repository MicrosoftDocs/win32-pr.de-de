---
title: Imstscaxevents onlogincomplete-Methode
description: Wird aufgerufen, wenn das Client Steuerelement nach der Anzeige des Windows-Anmelde Dialogfelds erfolgreich an einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) angemeldet ist.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Onlogincomplete-Methode Remotedesktopdienste
- Onlogincomplete-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onlogincomplete-Methode
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
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518056"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>Imstscaxevents:: onlogincomplete-Methode

Wird aufgerufen, wenn das Client Steuerelement nach der Anzeige des Windows-Anmelde Dialogfelds erfolgreich an einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) angemeldet ist.

## <a name="syntax"></a>Syntax


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass das Steuerelement die Anmeldung abgeschlossen hat

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie dieses Ereignis mit Visual Basic Skriptcode behandelt wird. In diesem Beispiel wird davon ausgegangen, dass das Steuerelement Objekt den Namen "MsRdpClient" hat.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).


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
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





