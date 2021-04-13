---
description: Die spfilenotify- \_ renameerror-Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Umbenennungs Vorgangs ein Fehler auftritt.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: SPFILENOTIFY_RENAMEERROR Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347248"
---
# <a name="spfilenotify_renameerror-message"></a>Spfilenotify \_ renameerror-Meldung

Die **spfilenotify- \_ renameerror** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Umbenennungs Vorgangs ein Fehler auftritt.


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur. Der **Win32Error** -Member der **FilePath** -Struktur gibt den Fehler an, der beim Umbenennungs Vorgang aufgetreten ist.

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine sollte eine der folgenden zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**fileOp- \_ Wiederholung**</dt> </dl> | Der Benutzer hat versucht, den Umbenennungs Vorgang erneut auszuführen.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**fileOp-über \_ springen**</dt> </dl>  | Der Benutzer hat den Vorgang zum Umbenennen von Dateien übersprungen.<br/>                                                                                                                                                                                                      |
| <dl> <dt>**fileOp- \_ Abbruch**</dt> </dl> | Stoppt den warteschlangencommit. [**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **false** zurück. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt erweiterte Fehlerinformationen zurück, z \_ . b \_ \_ \_ . "Fehler abgebrochen" (wenn der Benutzer abgebrochen wurde) oder "Fehler"<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

