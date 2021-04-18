---
description: Mit der Pause-Methode wird die aktuelle Erfassung vorübergehend beendet.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats::P ause-Methode (Netmon. h)
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
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361087"
---
# <a name="istatspause-method"></a>IStats::P ause-Methode

Mit der **Pause** -Methode wird die aktuelle Erfassung vorübergehend beendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl>  | Die Erfassung wurde bereits angehalten.<br/>                                                                                                    |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>   | Der NPP erfasst keine Daten. Ruft die [iStats:: Start](istats-start.md) -Methode auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>   | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl> | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.<br/>                                |



 

## <a name="remarks"></a>Bemerkungen

Während die Erfassung angehalten wird, werden neue Frames erst aufgezeichnet, wenn ein Aufrufe der [iStats:: Resume](istats-resume.md) -Methode die Erfassung neu startet.

Wenn Sie die **iStats::P ause** -Methode und die **iStats:: Resume** -Methode verwenden, um die Erfassung zu steuern, werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzufügen, sobald die Erfassung ausgeführt wird.

Zum Neustarten des Aufzeichnungs Aufrufes [iStats:: Resume](istats-resume.md). Um die Erfassung anzuhalten, nennen Sie [iStats:: Beendigung](istats-stop.md).

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

[IStats:: Resume](istats-resume.md)
</dt> <dt>

[IStats:: Start](istats-start.md)
</dt> <dt>

[IStats:: Beendigung](istats-stop.md)
</dt> </dl>

 

 




