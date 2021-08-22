---
description: Die SPFILENOTIFY FILEEXTRACTED-Benachrichtigung wird von SetupIterateCabinet an eine Rückrufroutine gesendet, um anzugeben, dass eine Datei aus der Schränkung extrahiert wurde oder dass eine Extraktion fehlgeschlagen ist und die Verarbeitung des Schränkes abgebrochen \_ wurde.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: SPFILENOTIFY_FILEEXTRACTED (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56b5028dec11cf2317be080fb82b79bf155be007c66abcbee33492aa229d6317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665110"
---
# <a name="spfilenotify_fileextracted-message"></a>SPFILENOTIFY \_ FILEEXTRACTED-Meldung

Die **SPFILENOTIFY \_ FILEEXTRACTED-Benachrichtigung** wird von [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) an eine Rückrufroutine gesendet, um anzugeben, dass eine Datei aus der Schränkung extrahiert wurde oder dass eine Extraktion fehlgeschlagen ist und die Verarbeitung des Schränkes abgebrochen wurde.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) die Pfadinformationen für die extrahierte Datei enthält. Das **SourceFile-Member** der **FILEPATHS-Struktur** enthält den vollständigen Quellpfad der Schränkung. Das **TargetFile-Mitglied** gibt den vollständigen Zielpfad der Datei an, die auf dem System installiert werden soll.

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine für die Schränkung sollte einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NO \_ ERROR**</dt> </dl>  | Es ist kein Fehler aufgetreten. Fahren Sie mit der Verarbeitung des Schränks fort.<br/>                                                                                                                                |
| <dl> <dt>**FEHLER \_ XXX**</dt> </dl> | Ein Fehler des angegebenen Typs ist aufgetreten. [**SetupIterateCabinet gibt**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 0 (null) zurück. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den angegebenen Fehlercode zurück.<br/> |



 

> [!Note]  
> Die Setup-API enthält keine standardmäßige Rückrufroutine für die Schränkung. Ihre Setupanwendung sollte eine Rückrufroutine zur Handhabung der von der [**SetupIterateCabinet-Funktion gesendeten Benachrichtigungen**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) liefern.

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

