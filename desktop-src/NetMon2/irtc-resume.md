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
ms.openlocfilehash: f8b8cebaf14f5e6a42a938a8fe585934137a899f8afaeb2d28533c0c0cfa18b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742980"
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

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE NOT PAUSED (NMERR-ERFASSUNG NICHT \_ \_ ANGEHALTEN)**</dt> </dl> | Die Erfassung wird nicht angehalten. Rufen [Sie IRTC::P ause auf,](irtc-pause.md) um die Erfassung anzuhalten.<br/>                                |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>       | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IRTC::Verbinden](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>        | Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Verbinden-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Daten erst erfasst, wenn ein Aufruf der [IRTC::Resume-Methode](idelaydc-resume.md) die Erfassung neu startet.

Wenn Sie die **Methoden Anhalten** **und** Fortsetzen verwenden, um [](c.md) die Erfassung zu steuern, fügt Netzwerkmonitor weiterhin Konversationsstatistiken zu den vorhandenen Statistiken für die aktuelle Erfassung hinzu.

Um die Erfassung zu beenden, rufen Sie die [IRTC::Stop-Methode](irtc-stop.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




