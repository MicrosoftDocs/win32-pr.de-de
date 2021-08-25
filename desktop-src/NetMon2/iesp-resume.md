---
description: 'IESP::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: IESP::Resume-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: dd39cb83c90c566f0022679e70680e916daeb2a43a4d62e993e096930ee2f14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890470"
---
# <a name="iespresume-method"></a>IESP::Resume-Methode

Die **Resume-Methode** startet eine angehaltene Erfassung neu.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt> </dl> | Die Erfassung wird nicht angehalten. Rufen Sie [**IESP::P ause**](iesp-pause.md) auf, um die Erfassung anzuhalten.<br/>                        |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>       | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [**IESP::Verbinden**](iesp-connect.md) auf, um eine Verbindung mit dem Netzwerk herzustellen.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>             | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [**IESP::Verbinden-Methode.**](iesp-connect.md)<br/>            |



 

## <a name="remarks"></a>Hinweise

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn **IESP::Resume** aufgerufen wird, um die Erfassung neu zu starten. Wenn **Anhalten** und **Fortsetzen** verwendet werden, um die Erfassung zu beenden und neu zu starten, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.

Wenn **Sie Anhalten** und **Fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.

Rufen Sie [**IESP::Stop**](iesp-stop.md)auf, um die Erfassung zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP::Verbinden**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP::Stop**](iesp-stop.md)
</dt> </dl>

 

 




