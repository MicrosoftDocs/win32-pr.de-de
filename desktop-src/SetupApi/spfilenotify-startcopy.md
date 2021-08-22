---
description: Die SPFILENOTIFY STARTCOPY-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die \_ Warteschlange einen Dateikopiervorgang startet.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: SPFILENOTIFY_STARTCOPY (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73be97df5b0241246131ad8dfec1bb67a76c439d8a40eb034446a33b0a9a95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664772"
---
# <a name="spfilenotify_startcopy-message"></a>SPFILENOTIFY \_ STARTCOPY-Meldung

Die **SPFILENOTIFY \_ STARTCOPY-Benachrichtigung** wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Dateikopiervorgang startet.


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Hat immer den Wert FILEOP \_ COPY.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine sollte einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Bricht den Warteschlangen-Commitprozess ab. Die Rückrufroutine sollte [**SetLastError aufrufen,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) um den Grund für die Beendigung anzugeben. Die [**SetupCommitFileQueue-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **FALSE** zurück, und ein nachfolgender Aufruf von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode zurück, der von der Rückrufroutine während des Aufrufs von **SetLastError festgelegt wurde.**<br/> |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Führen Sie den Dateikopiervorgang aus.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | Überspringen Sie den aktuellen Kopiervorgang.<br/>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
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

 

