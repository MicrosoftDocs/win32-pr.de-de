---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStats:: Resume-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867020"
---
# <a name="istatsresume-method"></a>IStats:: Resume-Methode

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



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>       | Der npp ist nicht mit dem Netzwerk verbunden.<br/>                                                                                          |
| <dl> <dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt> </dl> | Die Erfassung wird nicht angehalten. Nennen Sie die [iStats::P ause](istats-pause.md) -Methode, um die Erfassung vorübergehend anzuhalten.<br/>                     |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>       | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl>     | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.<br/>                                |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung im angehaltenen Zustand befindet, werden neue Daten erst aufgezeichnet, wenn die iStats:: Resume-Methode aufgerufen wird, um die Erfassung neu zu starten.

Bei der Verwendung der Methoden  **zum Anhalten und fort** setzen zum Steuern der Erfassung werden von Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzugefügt.

Um die Erfassung anzuhalten, nennen Sie [iStats:: Beendigung](istats-stop.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats:: Beendigung](istats-stop.md)
</dt> </dl>

 

 




