---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP:: Resume-Methode (Netmon. h)'
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
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343227"
---
# <a name="iespresume-method"></a>IESP:: Resume-Methode

Mit der **Resume** -Methode wird eine angehaltene Erfassung neu gestartet.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt> </dl> | Die Erfassung wird nicht angehalten. Wenden Sie [**iESP an::P ause**](iesp-pause.md) , um die Erfassung anzuhalten.<br/>                        |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>       | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [**iESP:: Connect**](iesp-connect.md) an, um eine Verbindung mit dem Netzwerk herzustellen.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>             | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**iESP:: Connect**](iesp-connect.md) -Methode.<br/>            |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung im angehaltenen Zustand befindet, werden der aktuellen [*Erfassungs Datei*](c.md) keine neuen Daten hinzugefügt, bis **iESP:: Resume** aufgerufen wird, um die Erfassung neu zu starten. Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu **beenden und neu** zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.

Bei der **Verwendung** von **Anhalten und fort** setzen zur Steuerung der Erfassung werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzufügen.

Um die Erfassung anzuhalten, nennen Sie [**iESP:: Beendigung**](iesp-stop.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP:: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: Beendigung**](iesp-stop.md)
</dt> </dl>

 

 




