---
description: 'IESP::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP::P ause-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3727bbabe9c56620b313d70ed529b5ac5f43bed620e98e49a3f6c3564fd1ba3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063960"
---
# <a name="iesppause-method"></a>IESP::P ause-Methode

Die **Pause-Methode** hält die aktuelle Erfassung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpStats* 
</dt> <dd>

Veraltet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung ist bereits angehalten.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>  | Das NPP erfasst keine Daten. Rufen Sie [IESP::Start](iesp-start.md) auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IESP::Verbinden](iesp-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>        | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IESP::Verbinden-Methode.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn Sie die [IESP::Resume-Methode](iesp-resume.md) aufrufen, um die Erfassung neu zu starten. Wenn **Anhalten** und **Fortsetzen** verwendet werden, um die Erfassung zu beenden und neu zu starten, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.

Wenn Sie die **Methoden IESP::P ause** und **IESP::Resume** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.

Rufen Sie [IESP::Resume](iesp-resume.md)auf, um die Erfassung neu zu starten. Rufen Sie [IESP::Stop](iesp-stop.md)auf, um die Erfassung zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Verbinden](iesp-connect.md)
</dt> <dt>

[IESP::Resume](iesp-resume.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




