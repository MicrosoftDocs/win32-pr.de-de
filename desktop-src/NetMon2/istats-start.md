---
description: Die Start-Methode startet eine Aufzeichnung.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStats:: Start-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863035"
---
# <a name="istatsstart-method"></a>IStats:: Start-Methode

Die **Start** -Methode startet eine Aufzeichnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl>  | Die Erfassung wurde angehalten und muss beendet werden, bevor Sie neu gestartet werden kann. Zum Abbrechen der Erfassung wird die [iStats:: stopmethode](istats-stop.md) aufgerufen.<br/> |
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>        | Die Erfassung wurde bereits gestartet.<br/>                                                                                                            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>   | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.<br/>           |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl> | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.<br/>                                          |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Erfassung mit der iStats:: Start-Methode und der [iStats:: beenden](istats-stop.md) -Methode neu starten, müssen Sie die [iStats:: Configure](istats-configure.md) -Methode zum Neukonfigurieren der Verbindung bei jedem Aufruf von iStats:: Start zum Neustarten der Datenerfassung verwenden.

> [!Note]  
> Sie können die Erfassung auch starten und Abbrechen, indem Sie die [iStats::P ause](istats-pause.md) -Methode und die [iStats:: Resume](istats-resume.md) -Methode verwenden. Wenn Sie diese Methoden verwenden, werden die erfassten Daten in derselben Erfassungs Datei gespeichert.

 

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

[IStats:: Configure](istats-configure.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats:: Resume](istats-resume.md)
</dt> <dt>

[IStats:: Beendigung](istats-stop.md)
</dt> </dl>

 

 




