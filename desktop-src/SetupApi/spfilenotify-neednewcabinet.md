---
description: Die spfilenotify \_ neednewcab-Benachrichtigung wird von setupiteratecabinet gesendet, um anzugeben, dass die aktuelle Datei in einer anderen CAB-Datei fortgesetzt wird.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: SPFILENOTIFY_NEEDNEWCABINET Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218175"
---
# <a name="spfilenotify_neednewcabinet-message"></a>Spfilenotify \_ neednewcab-Nachricht

Die **spfilenotify \_ neednewcab** -Benachrichtigung wird von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) gesendet, um anzugeben, dass die aktuelle Datei in einer anderen CAB-Datei fortgesetzt wird. Die Rückruf Routine kann dann [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)aufrufen oder ein eigenes Dialogfeld erstellen, in dem der Benutzer aufgefordert wird, den nächsten Datenträger einzufügen.


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Ein Zeiger auf eine CAB [**-Informationsstruktur \_**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) , die Informationen über die CAB-Datei und die zu extrahierende Datei enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Wenn der Rückruf keinen Fehler zurückgibt \_ , ist dieser Parameter ein Zeiger auf eine NULL-terminierte Zeichenfolge. Wenn die Zeichenfolge nicht leer ist, wird ein neuer Pfad zur CAB-Datei angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Routine sollte einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                 | Beschreibung                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**kein \_ Fehler**</dt> </dl>    | Es wurde kein Fehler gefunden. setzen Sie die Verarbeitung der CAB-<br/>                                                                                                                                                                        |
| <dl> <dt>**Fehler \_* XXX * * *</dt> </dl> | Ein Fehler des angegebenen Typs ist aufgetreten. Die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion gibt " **false**" zurück, und der angegebene Fehlercode wird durch einen get-Befehl von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" zurückgegeben.<br/> |



 

> [!Note]  
> Es ist keine standardmäßige CAB-Rückruf Routine vorhanden. Daher müssen Sie eine Rückruf Routine bereitstellen, um die von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendeten Benachrichtigungen zu verarbeiten.

 

## <a name="remarks"></a>Bemerkungen

Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , prüft [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) den Puffer, auf den von *Param2* verwiesen wird. Wenn der Puffer nicht leer ist, enthält er einen neuen Quellpfad. Wenn der Puffer leer ist, wird davon ausgegangen, dass der Quellpfad unverändert ist.

Die Rückruffunktion sollte sicherstellen, dass auf die CAB-Datei zugegriffen werden kann, bevor Sie zurückkehrt, und die Funktion [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) aufrufen, wenn neue Medien eingefügt werden müssen.

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

[**CAB- \_ Informationen**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**Setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

