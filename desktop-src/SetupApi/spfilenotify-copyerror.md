---
description: Die spfilenotify- \_ copyError-Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Kopiervorgangs ein Fehler auftritt.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: SPFILENOTIFY_COPYERROR Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865715"
---
# <a name="spfilenotify_copyerror-message"></a>Spfilenotify- \_ copyError-Meldung

Die **spfilenotify- \_ copyError** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Kopiervorgangs ein Fehler auftritt.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.

</dd> <dt>

*Param2* 
</dt> <dd>

Zeiger auf einen Puffer mit einer Größe von Max. \_ Pfad Zeichen, der neue Pfadinformationen speichert, die vom Benutzer angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückruf muss einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**fileOp- \_ Abbruch**</dt> </dl>   | Die Warteschlangen Verarbeitung sollte abgebrochen werden. [**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt 0 (null) zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt erweiterte Fehlerinformationen zurück, wie z. b. \_ den Fehler abgebrochen (wenn der Benutzer abgebrochen hat) oder einen Fehler \_ \_ \_<br/> |
| <dl> <dt>**fileOp \_ NewPath**</dt> </dl> | Wiederholen Sie den Kopiervorgang mit dem Pfad der Rückruffunktion, die im Puffer platziert wurde, auf den der *Param2* -Parameter verweist. Die Rückruf Routine sollte sicherstellen, dass der Pfad die Puffergröße eines TCHAR-Arrays von Max- \_ Pfad Elementen nicht überflutet.<br/>                |
| <dl> <dt>**fileOp- \_ Wiederholung**</dt> </dl>   | Der Benutzer versucht erneut, den Kopiervorgang auszuführen.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**fileOp-über \_ springen**</dt> </dl>    | Der Benutzer wird den Datei Kopiervorgang übersprungen.<br/>                                                                                                                                                                                                                      |



 

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

 

