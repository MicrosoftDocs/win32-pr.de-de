---
description: 'Weitere Informationen finden Sie unter: Funktionen der Cabinet-API.'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funktionen der Cabinet-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668354"
---
# <a name="cabinet-api-functions"></a>Funktionen der Cabinet-API

In diesem Abschnitt werden die folgenden Funktionen der Cabinet-API beschrieben:

## <a name="fci-functions"></a>FCI-Funktionen

Die FCI-Bibliothek (File Compression Interface, Dateikomprimierungsschnittstelle) bietet die Möglichkeit, Cab-Dateien (auch als "CAB-Dateien" bezeichnet) zu erstellen. Darüber hinaus bietet die Bibliothek eine Komprimierung, um die Größe der in Schränken gespeicherten Dateidaten zu reduzieren.



| Funktion                                   | Beschreibung                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Fügt dem aktuell zusammenfügten Schränk eine Datei hinzu.<br/>                                           |
| [**FCIErzeugen**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Erstellt einen FCI-Kontext.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Löscht einen geöffneten FCI-Kontext und gibt alle speicher- und temporären Dateien frei, die dem Kontext zugeordnet sind.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Schließt die aktuelle Schränkung ab.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Erzwingt, dass der aktuelle Ordner, der erstellt wird, sofort abgeschlossen wird.<br/>                        |



 

## <a name="fdi-functions"></a>FDI-Funktionen

Die FDI-Bibliothek (File Decompression Interface, Dateidekomprimierungsschnittstelle) bietet die Möglichkeit, Dateien aus Schränken zu extrahieren.



| Funktion                                         | Beschreibung                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrahiert Dateien aus Schränken.<br/>                                                          |
| [**FDIErzeugen**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Erstellt einen FDI-Kontext.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Löscht einen geöffneten FDI-Kontext.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Bestimmt, ob es sich bei einer Datei um eine Schränkung handelt, und gibt beschreibende Informationen zurück.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Schneidt eine Ablagedatei ab der angegebenen Ordnernummer ab.<br/>                      |



 

## <a name="deprecated-functions"></a>Veraltete Funktionen

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Extract**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Cabinet-API](cabinet-api-reference.md)
</dt> <dt>

[Verwenden der Cabinet-API](using-the-cabinet-api.md)
</dt> </dl>

 

 




