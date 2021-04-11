---
description: Da die Setup-API keine standardmäßige CAB-Rückruf Routine bereitstellt, müssen Sie eine Routine bereitstellen. Die Rückruf Routine, die für die setupiteratecabinet-Funktion erforderlich ist, muss dieselbe Form aufweisen wie die, auf die von filecallback verwiesen wird.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Erstellen einer CAB-Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216336"
---
# <a name="creating-a-cabinet-callback-routine"></a>Erstellen einer CAB-Rückruf Routine

Da die Setup-API keine standardmäßige CAB-Rückruf Routine bereitstellt, müssen Sie eine Routine bereitstellen. Die Rückruf Routine, die für die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion erforderlich ist, muss dieselbe Form aufweisen wie die, auf die von [filecallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)verwiesen wird.

Im folgenden finden Sie die Syntax, die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) verwendet, um eine Benachrichtigung an die Rückruf Routine zu senden.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Der *Kontext* Parameter ist ein void-Zeiger auf eine Kontext Variable oder-Struktur, die von der Rückruf Routine verwendet werden kann, um Informationen zu speichern, die zwischen nachfolgenden Aufrufen der Rückruf Routine beibehalten werden müssen.

Die Implementierung dieses Kontexts wird durch die Rückruf Routine angegeben und nie von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)referenziert oder geändert.

Der *Benachrichtigungs* Parameter ist eine Ganzzahl ohne Vorzeichen und hat einen der folgenden Werte.



| Benachrichtigung                                                        | Beschreibung                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**spfilenotifizieren von \_ fileextrahierung**](spfilenotify-fileextracted.md)   | Die Datei wurde aus der CAB-Datei extrahiert.      |
| [**spfilenotify \_ filinput Cabinet**](spfilenotify-fileincabinet.md)   | In der CAB-Datei ist eine Datei aufgetreten.              |
| [**spfilenotify \_ neednewcabinet**](spfilenotify-neednewcabinet.md) | Die aktuelle Datei wird in der nächsten CAB-Datei fortgesetzt. |



 

Die letzten zwei Parameter, *param1* und *Param2*, sind auch ganze Zahlen ohne Vorzeichen und enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind. Weitere Informationen zu den von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendeten Benachrichtigungen finden Sie unter CAB- [Datei Benachrichtigungen](cabinet-file-notifications.md).

Eine SP- \_ Datei \_ Benachrichtigungs \_ Rückruf-Routine gibt eine ganze Zahl ohne Vorzeichen zurück. Die CAB-Rückruf Routine sollte abhängig von der Benachrichtigung einen der folgenden Werte zurückgeben.

Für die spfilenotify \_ fileincabinet-Benachrichtigung erwartet [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , dass einer der folgenden Werte von der Rückruf Routine zurückgegeben wird.



| Wert         | Bedeutung                   |
|---------------|---------------------------|
| fileOp- \_ Abbruch | Abbrechen der CAB-Verarbeitung. |
| fileOp- \_ doit  | Extrahieren Sie die aktuelle Datei. |
| fileOp-über \_ springen  | Überspringen Sie die aktuelle Datei.    |



 

Für spfilenotify \_ neednewcab-und spfilenotify- \_ fileextrahierte Benachrichtigungen erwartet **setupiteratecabinet** , dass einer der folgenden Werte von der Rückruf Routine zurückgegeben wird.



| Wert      | Bedeutung                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| kein \_ Fehler  | Es wurde kein Fehler gefunden. setzen Sie die Verarbeitung der CAB-                                                                                                                                                                        |
| Fehler \_ xxx | Ein Fehler des angegebenen Typs ist aufgetreten. Die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion gibt " **false**" zurück, und der angegebene Fehlercode wird durch einen get-Befehl von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" zurückgegeben. |



 

Wenn die Rückruf Routine fileOp \_ doit zurückgibt, muss die Routine auch einen vollständigen Zielpfad bereitstellen. Weitere Informationen finden Sie unter [**spfilenotify \_ fileincabinet**](spfilenotify-fileincabinet.md).

 

 
