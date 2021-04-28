---
description: 'IDelaydC::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: IDelaydC::P ause-Methode (Netmon.h)
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
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098498"
---
# <a name="idelaydcpause-method"></a>IDelaydC::P ause-Methode

Die **Pause-Methode** hält die aktuelle Erfassung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung befindet sich bereits in einem angehaltenen Zustand.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>  | Das NPP erfasst keine Daten. Rufen Sie [IDelaydC::Start](idelaydc-start.md) auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>    | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn die **IDelaydC::Resume-Methode** aufgerufen wird, um die Erfassung neu zu starten. Wenn **Anhalten** und **Fortsetzen** zum Beenden und Neustarten der Erfassung verwendet werden, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.

Wenn **Sie IDelaydC::P ause** und **IDelaydC::Resume** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.

Um die Erfassung neu zu starten, rufen [Sie IDelaydC::Resume auf.](idelaydc-resume.md)

Um die Erfassung zu beenden, rufen [Sie IDelaydC::Stop](idelaydc-stop.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




