---
description: Die spfilenotify- \_ Datei extrahierte Benachrichtigung wird von setupiteratecabinet an eine Rückruf Routine gesendet, um anzugeben, dass eine Datei aus der CAB-Datei extrahiert wurde oder dass eine Extraktion fehlgeschlagen ist und die CAB-Verarbeitung abgebrochen wurde.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: SPFILENOTIFY_FILEEXTRACTED Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363384"
---
# <a name="spfilenotify_fileextracted-message"></a>Spfilenotify \_ fileextrahierte Meldung

Die **spfilenotify- \_ Datei extrahierte** Benachrichtigung wird von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) an eine Rückruf Routine gesendet, um anzugeben, dass eine Datei aus der CAB-Datei extrahiert wurde oder dass eine Extraktion fehlgeschlagen ist und die CAB-Verarbeitung abgebrochen wurde.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Pfadinformationen für die extrahierte Datei enthält. Der **SourceFile** -Member der **FilePath** -Struktur enthält den vollständigen Quellpfad der CAB-Datei. Der **targetfile** -Member liefert den vollständigen Zielpfad der Datei, die auf dem System installiert werden soll.

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die CAB-Rückruf Routine muss einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**kein \_ Fehler**</dt> </dl>  | Es wurde kein Fehler gefunden. setzen Sie die Verarbeitung der CAB-<br/>                                                                                                                                |
| <dl> <dt>**Fehler \_ xxx**</dt> </dl> | Ein Fehler des angegebenen Typs ist aufgetreten. [**Setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) gibt 0 (null) zurück. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den angegebenen Fehlercode zurück.<br/> |



 

> [!Note]  
> Mit der Setup-API wird keine standardmäßige CAB-Rückruf Routine bereitgestellt. Die Setup Anwendung sollte eine Rückruf Routine bereitstellen, um die Benachrichtigungen zu verarbeiten, die von der [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion gesendet werden.

 

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

[**Setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

