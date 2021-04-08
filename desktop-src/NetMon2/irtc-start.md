---
description: Die Start-Methode startet die Erfassung.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Untc:: Start-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864064"
---
# <a name="irtcstart-method"></a>Untc:: Start-Methode

Die **Start** -Methode startet die Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl> | Die Erfassung befindet sich im angehaltenen Zustand und muss beendet werden, bevor Sie neu gestartet werden kann. Zum Abbrechen der Erfassung wird der Befehl " [untc:: Beendigung](idelaydc-stop.md) " aufgerufen.<br/> |
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>       | Die Erfassung wurde bereits gestartet.<br/>                                                                                                            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>  | Der npp ist nicht mit dem Netzwerk verbunden. Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.<br/>                         |
| <dl> <dt>**nmerr \_ nicht in \_ Echtzeit**</dt> </dl>   | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Erfassung mit den Methoden "untc:: Start" und " [untc:: beenden](irtc-stop.md) " neu starten, müssen Sie die Methode " [iritc:: Configure](irtc-configure.md) " zum erneuten Konfigurieren der Verbindung bei jedem Aufruf von "untc:: Start" zum Neustarten der Datenerfassung verwenden.

> [!Note]  
> Sie können die Erfassung auch starten und Abbrechen, indem Sie die Methoden " [untc::P ause](irtc-pause.md) " und " [untc:: Resume](irtc-resume.md) " verwenden.

 

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

["Iran:: Configure"](irtc-configure.md)
</dt> <dt>

[Iran:: Connect](irtc-connect.md)
</dt> <dt>

[Iran::P ause](irtc-pause.md)
</dt> <dt>

[Iran:: Resume](irtc-resume.md)
</dt> <dt>

[Iran:: Beendigung](irtc-stop.md)
</dt> </dl>

 

 




