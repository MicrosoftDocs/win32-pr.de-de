---
description: Die Pause-Methode hält die aktuelle Erfassung an.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Idelta-DC::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861995"
---
# <a name="idelaydcpause-method"></a>Idelta aydc::P ause-Methode

Die **Pause** -Methode hält die aktuelle Erfassung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl> | Die Erfassung befindet sich bereits im angehaltenen Zustand.<br/>                                                                                  |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>  | Der NPP erfasst keine Daten. Wenden Sie [idelta-DC:: Start](idelaydc-start.md) an, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>  | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ verzögert**</dt> </dl>    | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung im angehaltenen Zustand befindet, werden der aktuellen [*Erfassungs Datei*](c.md) keine neuen Daten hinzugefügt, bis die **idelta-DC:: Resume** -Methode aufgerufen wird, um die Erfassung neu zu starten. Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu **beenden und neu** zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.

Bei der Verwendung von **idelta aydc::P ause** und **idelta aydc:: Resume** zum Steuern der Erfassung werden von Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzugefügt, wenn die Erfassung ausgeführt wird.

Um die Erfassung neu zu starten, nennen Sie [idelta aydc:: Resume](idelaydc-resume.md).

Um die Erfassung anzuhalten, nennen Sie [idelta aydc:: Stop.](idelaydc-stop.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

[Idelta aydc:: Connect](idelaydc-connect.md)
</dt> <dt>

[Idelta aydc:: Resume](idelaydc-resume.md)
</dt> <dt>

[Idelta aydc:: Start](idelaydc-start.md)
</dt> <dt>

[Idelta aydc:: Beendigung](idelaydc-stop.md)
</dt> </dl>

 

 




