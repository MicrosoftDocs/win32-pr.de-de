---
description: Die spfilenotify \_ targetneuere-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei in die Warteschlange eingereiht ist, wenn die zu kopierende Datei den SP \_ -Kopiervorgang \_ neuer oder \_ eine neuere \_ \_ Version des SP-Kopiervorgangs enthält
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: SPFILENOTIFY_TARGETNEWER Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362300"
---
# <a name="spfilenotify_targetnewer-message"></a>\_Spfilenotifiktargetneuere Nachricht

Die **spfilenotify \_ targetneuere** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei in die Warteschlange eingereiht ist, wenn die zu kopierende Datei den SP \_ -Kopiervorgang \_ neuer oder \_ eine neuere \_ \_ Version des SP-Kopiervorgangs enthält Er kann mit dem [**spfilenotify-Element " \_ langmismatch**](spfilenotify-langmismatch.md) " und/oder " [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md)" allein an die Rückruf Routine oder "ORed" gesendet werden.


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Informationen zu den Pfaden für Quell-und Zieldateien enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Dieser Parameter wird nicht verwendet, es sei denn, diese Benachrichtigung wird mithilfe des OR-Operators mit [**spfilenotify \_ langmismatch**](spfilenotify-langmismatch.md)kombiniert.

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

 

 




