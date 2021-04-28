---
description: 'IRTC::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC::P ause-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110678"
---
# <a name="irtcpause-method"></a>IRTC::P ause-Methode

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



| Rückgabecode                                                                                           | Beschreibung                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung ist bereits angehalten.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>  | Das NPP erfasst keine Daten. Rufen Sie [IRTC::Start](irtc-start.md) auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Frames erst erfasst, wenn die [IRTC::Resume-Methode](irtc-resume.md) aufgerufen wird, um die Erfassung neu zu starten.

Wenn Sie die **Methoden IRTC::P ause** und **IRTC::Resume** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.

Um den Aufzeichnungsaufruf neu zu starten, rufen [Sie IRTC::Resume auf.](irtc-resume.md) Um die Erfassung zu beenden, rufen Sie [IRTC::Stop](irtc-stop.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




