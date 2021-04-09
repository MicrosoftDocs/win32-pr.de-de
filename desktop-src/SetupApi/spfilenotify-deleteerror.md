---
description: Die spfilenotify \_ deleteerror-Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Löschvorgangs ein Fehler auftritt.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: SPFILENOTIFY_DELETEERROR Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050520"
---
# <a name="spfilenotify_deleteerror-message"></a>Spfilenotify \_ deleteerror-Meldung

Die **spfilenotify \_ deleteerror** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Löschvorgangs ein Fehler auftritt.


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine muss einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**fileOp- \_ Abbruch**</dt> </dl> | Die Warteschlangen Verarbeitung sollte abgebrochen werden. [**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt 0 (null) zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt erweiterte Fehlerinformationen zurück, wie z. b. \_ den Fehler abgebrochen (wenn der Benutzer abgebrochen hat) oder einen Fehler \_ \_ \_<br/> |
| <dl> <dt>**fileOp- \_ Wiederholung**</dt> </dl> | Der Benutzer versucht erneut, den Löschvorgang auszuführen.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**fileOp-über \_ springen**</dt> </dl>  | Der Benutzer wird den Datei Löschvorgang übersprungen.<br/>                                                                                                                                                                                                                    |



 

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

 

