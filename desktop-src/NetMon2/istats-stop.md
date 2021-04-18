---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStats:: stopmethode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345772"
---
# <a name="istatsstop-method"></a>IStats:: stopmethode

Die Methode " **Beenden** " beendet die aktuelle Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>   | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>   | Der NPP erfasst keine Daten. Ruft die [iStats:: Start](istats-start.md) -Methode auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl> | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.<br/>                                |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Erfassung nach dem Aufrufen von **iStats:: beenden** neu starten, stellen Sie sicher, dass Sie jedes Mal, wenn Sie [iStats:: Start](istats-start.md) aufrufen, die [iStats:: Configure](istats-configure.md) -Methode aufrufen, um die Erfassung neu zu starten.

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

[IStats:: Configure](istats-configure.md)
</dt> <dt>

[IStats:: Start](istats-start.md)
</dt> </dl>

 

 




