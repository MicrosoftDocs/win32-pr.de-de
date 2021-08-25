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
ms.openlocfilehash: dfe48afce1e8fd2350f1d1b696eb426a326ade1b30151e872afee30c0ed997f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910510"
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
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IDelaydC::Verbinden](idelaydc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>    | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Verbinden-Methode.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn die **IDelaydC::Resume-Methode** aufgerufen wird, um die Erfassung neu zu starten. Wenn **Anhalten** und **Fortsetzen** verwendet werden, um die Erfassung zu beenden und neu zu starten, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.

Wenn **Sie IDelaydC::P ause** und **IDelaydC::Resume** zum Steuern der Erfassung verwenden, fügen Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.

Um die Erfassung neu zu starten, rufen [Sie IDelaydC::Resume auf.](idelaydc-resume.md)

Um die Erfassung zu beenden, rufen [Sie IDelaydC::Stop](idelaydc-stop.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Verbinden](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




