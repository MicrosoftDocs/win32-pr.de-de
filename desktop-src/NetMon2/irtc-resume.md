---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'Untc:: Resume-Methode (Netmon. h)'
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
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343825"
---
# <a name="irtcresume-method"></a>Untc:: Resume-Methode

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



| Rückgabecode                                                                                                | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt> </dl> | Die Erfassung wird nicht angehalten. Wenden Sie die [:P ause](irtc-pause.md) an, um die Erfassung anzuhalten.<br/>                                |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>       | Der npp ist nicht mit dem Netzwerk verbunden. Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht in \_ Echtzeit**</dt> </dl>        | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Daten erst aufgezeichnet, wenn ein Aufrufe der Methode " [untc:: Resume](idelaydc-resume.md) " die Erfassung neu startet.

Bei der Verwendung der Methoden  **zum Anhalten und fort** setzen zum Steuern der Erfassung werden von Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzugefügt.

Um die Erfassung zu verhindern, wenden Sie die Methode " [untc:: stopand](irtc-stop.md) " an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Iran"](irtc.md)
</dt> <dt>

[Iran:: Connect](irtc-connect.md)
</dt> <dt>

[Iran::P ause](irtc-pause.md)
</dt> <dt>

[Iran:: Beendigung](irtc-stop.md)
</dt> </dl>

 

 




