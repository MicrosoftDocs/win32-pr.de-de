---
description: 'IRTC::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: IRTC::Resume-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 55e5cb66eecbee96df9573e9347d1f32e3508d2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110562"
---
# <a name="irtcresume-method"></a>IRTC::Resume-Methode

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



| Rückgabecode                                                                                                | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt> </dl> | Die Erfassung wird nicht angehalten. Rufen Sie [IRTC::P ause](irtc-pause.md) auf, um die Erfassung anzuhalten.<br/>                                |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>       | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>        | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Daten erst erfasst, wenn die Erfassung durch einen Aufruf der [IRTC::Resume-Methode](idelaydc-resume.md) neu gestartet wird.

Wenn Sie die Methoden **Anhalten** und **Fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.

Um die Erfassung zu beenden, rufen Sie die [IRTC::Stop-Methode](irtc-stop.md) auf.

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

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




