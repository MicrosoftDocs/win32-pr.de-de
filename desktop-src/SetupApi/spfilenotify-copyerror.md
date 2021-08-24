---
description: Die SPFILENOTIFY \_ COPYERROR-Benachrichtigung wird an die Rückrufroutine gesendet, wenn während eines Dateikopiervorgangs ein Fehler auftritt.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: SPFILENOTIFY_COPYERROR Meldung (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80160af9d8053a90c1848d397da6bbb9bf41f2793756e1d5491fb0d6f5e39abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665150"
---
# <a name="spfilenotify_copyerror-message"></a>SPFILENOTIFY \_ COPYERROR-Meldung

Die **SPFILENOTIFY \_ COPYERROR-Benachrichtigung** wird an die Rückrufroutine gesendet, wenn während eines Dateikopiervorgangs ein Fehler auftritt.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Zeiger auf einen Puffer der Größe MAX \_ PATH-Zeichen, in dem vom Benutzer angegebene neue Pfadinformationen gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückruf sollte einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl>   | Die Warteschlangenverarbeitung sollte abgebrochen werden. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt 0 (null) und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) erweiterte Fehlerinformationen wie ERROR \_ CANCELLED (wenn der Benutzer abgebrochen hat) oder ERROR \_ NOT ENOUGH MEMORY \_ \_ zurück.<br/> |
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | Wiederholen Sie den Kopiervorgang unter Verwendung des Pfads, auf den die Rückruffunktion im Puffer platziert wird, auf den der *Parameter Param2* zeigt. Die Rückrufroutine sollte sicherstellen, dass der Pfad nicht die Puffergröße eines TCHAR-Arrays von MAX \_ PATH-Elementen überläuft.<br/>                |
| <dl> <dt>**\_FILEOP-WIEDERHOLUNG**</dt> </dl>   | Der Benutzer versucht erneut, den Kopiervorgang zu erstellen.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | Der Benutzer überspringt den Dateikopiervorgang.<br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

