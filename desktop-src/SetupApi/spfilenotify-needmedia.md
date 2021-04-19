---
description: Die spfilenotifitifimedia- \_ Benachrichtigung wird an die Rückruf Routine gesendet, wenn neue Medien oder eine neue CAB-Datei erforderlich sind.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: SPFILENOTIFY_NEEDMEDIA Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361761"
---
# <a name="spfilenotify_needmedia-message"></a>Spfilenotify- \_ needmedia-Meldung

Die **spfilenotifitifimedia \_** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn neue Medien oder eine neue CAB-Datei erforderlich sind.


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**Quell \_ Medien**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) Struktur.

</dd> <dt>

*Param2* 
</dt> <dd>

Zeiger auf ein Zeichen Array zum Speichern neuer Pfadinformationen, die vom Benutzer bereitgestellt werden. Die Puffergröße ist ein **TCHAR** -Array mit maximalen \_ Pfad Elementen. Die von der Setup Anwendung zurückgegebenen Pfadinformationen sollten diese Größe nicht überschreiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine sollte eine der folgenden zurückgeben.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**fileOp \_ NewPath**</dt> </dl> | Die Medien sind vorhanden, und die angeforderte Datei ist in dem Pfad verfügbar, der in dem Puffer angegeben ist, auf den *Param2* zeigt.<br/>                                                                                         |
| <dl> <dt>**fileOp-über \_ springen**</dt> </dl>    | Überspringen der angeforderten Datei<br/>                                                                                                                                                                                      |
| <dl> <dt>**fileOp- \_ Abbruch**</dt> </dl>   | Verarbeitung der Warteschlange abbrechen. Die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion gibt **false** zurück. GetLastError gibt erweiterte Fehlerinformationen zurück, z. b. einen Fehler, \_ Wenn der Benutzer abgebrochen wurde.<br/> |
| <dl> <dt>**fileOp-doit**</dt> </dl>     | Das Medium ist verfügbar.<br/>                                                                                                                                                                                      |



 

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

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**Quell \_ Medien**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




