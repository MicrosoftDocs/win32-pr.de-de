---
description: Die SPFILENOTIFY \_ TARGETEXISTS-Benachrichtigung wird an die Rückrufroutine gesendet, wenn die zu kopierende Datei mit dem SP \_ COPY NOOVERWRITE-Flag in die Warteschlange eingereiht wurde \_ und diese Datei bereits im Zielverzeichnis vorhanden ist.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: SPFILENOTIFY_TARGETEXISTS Meldung (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51f845d7ccb41b330f6365eff269645d08e58597e7e6dd3e9acc7a7f0300c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664740"
---
# <a name="spfilenotify_targetexists-message"></a>SPFILENOTIFY \_ TARGETEXISTS-Nachricht

Die **SPFILENOTIFY \_ TARGETEXISTS-Benachrichtigung** wird an die Rückrufroutine gesendet, wenn die zu kopierende Datei mit dem SP \_ COPY NOOVERWRITE-Flag in die Warteschlange eingereiht wurde \_ und diese Datei bereits im Zielverzeichnis vorhanden ist. Sie kann mithilfe des OR-Operators mit den Benachrichtigungen [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) und/oder [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) allein oder kombiniert an die Rückrufroutine gesendet werden.


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) die Informationen zu den Pfaden für die Quell- und Zieldateien enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Dieser Parameter wird nur verwendet, wenn diese Benachrichtigung mithilfe des OR-Operators mit der [**Benachrichtigung SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) kombiniert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine sollte einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>  | Überschreiben Sie die Datei im Zielverzeichnis.<br/> |
| <dl> <dt>**FALSE**</dt> </dl> | Überspringen Sie den aktuellen Kopiervorgang.<br/>            |



 

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
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




