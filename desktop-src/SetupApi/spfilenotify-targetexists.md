---
description: Die spfilenotify \_ targetexists-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei mit dem SP \_ Copy \_ noüberschreibungsflag in die Warteschlange eingereiht wurde und diese Datei bereits im Zielverzeichnis vorhanden ist.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: SPFILENOTIFY_TARGETEXISTS Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393714"
---
# <a name="spfilenotify_targetexists-message"></a>Spfilenotify \_ targetexists-Meldung

Die **spfilenotify \_ targetexists** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei mit dem SP \_ Copy \_ noüberschreibungsflag in die Warteschlange eingereiht wurde und diese Datei bereits im Zielverzeichnis vorhanden ist. Sie kann mithilfe des OR-Operators allein oder mithilfe des-Operators oder mit den [**spfilenotify- \_ Fehlern (spfilenotify**](spfilenotify-langmismatch.md) ) und/oder [**spfilenotify \_ targetneueren**](spfilenotify-targetnewer.md) -Benachrichtigungen an die Rückruf Routine gesendet werden.


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Informationen zu den Pfaden für die Quell-und Zieldateien enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Dieser Parameter wird nicht verwendet, es sei denn, diese Benachrichtigung wird mithilfe des OR-Operators mit der Benachrichtigung [**spfilenotify \_ langmismatch**](spfilenotify-langmismatch.md) kombiniert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine muss einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Überschreiben Sie die Datei im Zielverzeichnis.<br/> |
| <dl> <dt>**Alarm**</dt> </dl> | Überspringt den aktuellen Kopiervorgang.<br/>            |



 

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
</dt> <dt>

[**Setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**Setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**Setupinstallfrominf-Abschnitt**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




