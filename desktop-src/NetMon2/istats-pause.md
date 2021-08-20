---
description: Die Pause-Methode beendet vorübergehend die aktuelle Erfassung.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats::P ause-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d1bab0d66a081c175d997e093d7dd1ff2b0d1c9622ecff73e0b3b1473edc885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495210"
---
# <a name="istatspause-method"></a>IStats::P ause-Methode

Die **Pause-Methode** beendet vorübergehend die aktuelle Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl>  | Die Erfassung ist bereits angehalten.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>   | Das NPP erfasst keine Daten. Rufen Sie die [IStats::Start-Methode](istats-start.md) auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>   | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie die [IStats::Verbinden-Methode](istats-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ STATS \_ ONLY**</dt> </dl> | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IStats::Verbinden-Methode.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Hinweise

Während die Erfassung angehalten wird, werden neue Frames erst erfasst, wenn die Erfassung durch einen Aufruf der [IStats::Resume-Methode](istats-resume.md) neu gestartet wird.

Wenn Sie die Methoden **IStats::P ause** und **IStats::Resume** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.

So starten Sie den [Erfassungsaufruf IStats::Resume](istats-resume.md)neu. Rufen Sie [IStats::Stop](istats-stop.md)auf, um die Erfassung zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Verbinden](istats-connect.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Start](istats-start.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




