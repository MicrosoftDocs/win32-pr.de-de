---
description: Nachdem die INF-Datei geöffnet wurde, können Sie Informationen daraus sammeln, um die Benutzeroberfläche zu erstellen, oder den Installationsprozess weiterleiten. Die Setup-Funktionen bieten mehrere Ebenen der Funktionalität zum Sammeln von Informationen aus einer INF-Datei.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extrahieren von Dateiinformationen aus der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862999"
---
# <a name="extracting-file-information-from-the-inf-file"></a>Extrahieren von Dateiinformationen aus der INF-Datei

Nachdem die INF-Datei geöffnet wurde, können Sie Informationen daraus sammeln, um die Benutzeroberfläche zu erstellen, oder den Installationsprozess weiterleiten. Die Setup-Funktionen bieten mehrere Ebenen der Funktionalität zum Sammeln von Informationen aus einer INF-Datei.



| Um Informationen zu erfassen...                | Diese Funktionen verwenden...                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| Informationen zur INF-Datei                    | [**Setupgetinfinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**Setupqueryinffileinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**Setupqueryinfversioninformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa). |
| Informationen zu Quell-und Zieldateien         | [**Setupgetsourcefileloation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**Setupgetsourcefilesize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**Setupgettargetpath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**Setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| Aus einer Zeile einer INF-Datei            | [**Setupgetlinetext**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**Setupfindnextline**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**Setupfindnextmatchline**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**Setupgetlinebyindex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**Setupfindfirstline**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| Aus einem Feld einer Zeile in einer INF-Datei | [**Setupgetstringfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**Setupgetintfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**Setupgetbinaryfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**Setupgetmultiszfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

Im folgenden Beispiel wird die [**setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) -Funktion verwendet, um die lesbare Beschreibung eines Quell Mediums aus einer INF-Datei abzurufen.


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



Im Beispiel ist myinf das Handle der geöffneten INF-Datei. SourceID ist der Bezeichner für ein bestimmtes Quell Medium. Der Wert srcinfo \_ Description gibt an, dass die [**setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) -Funktion die Quell Medien Beschreibung abrufen soll. Der Puffer zeigt auf eine Zeichenfolge, die die Beschreibung empfängt, maxbufsize gibt die dem Puffer zugeordneten Ressourcen an, und "bufsize" gibt die Ressourcen an, die zum Speichern des Puffers benötigt werden.

Wenn "bufsize" größer als "maxbufsize" ist, gibt die Funktion " **false**" zurück, und ein nachfolgendes Aufrufen von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt einen fehlerhaften \_ Puffer zurück \_ .

 

 
