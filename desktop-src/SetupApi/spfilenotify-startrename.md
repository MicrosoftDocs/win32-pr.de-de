---
description: Die spfilenotify \_ startrename-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Vorgang zum Umbenennen von Dateien startet.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: SPFILENOTIFY_STARTRENAME Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c17d0c70b49ba00b3b16956e7ede5eda43b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351422"
---
# <a name="spfilenotify_startrename-message"></a>Spfilenotify- \_ startrename-Meldung

Die **spfilenotify \_ startrename** -Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Vorgang zum Umbenennen von Dateien startet.


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.

</dd> <dt>

*Param2* 
</dt> <dd>

Hat immer den Wert fileOp \_ Rename.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine muss einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**fileOp- \_ Abbruch**</dt> </dl> | Abbrechen des warteschlangencommit. Die Rückruf Routine sollte [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) aufrufen, um den Grund für die Beendigung anzugeben. [**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **false** zurück, und ein nachfolgendes Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode zurück, der von der Rückruf Routine während des Aufrufs von **SetLastError** festgelegt wurde.<br/> |
| <dl> <dt>**fileOp- \_ doit**</dt> </dl>  | Führen Sie den Datei Kopiervorgang aus.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**fileOp-über \_ springen**</dt> </dl>  | Überspringt den aktuellen Kopiervorgang.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

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

 

