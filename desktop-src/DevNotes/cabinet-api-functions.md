---
description: Weitere Informationen finden Sie in den CAB-API-Funktionen.
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: CAB-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860911"
---
# <a name="cabinet-api-functions"></a>CAB-API-Funktionen

In diesem Abschnitt werden die folgenden CAB-API-Funktionen beschrieben:

## <a name="fci-functions"></a>FCI-Funktionen

Die FCI (File Compression Interface)-Bibliothek bietet die Möglichkeit zum Erstellen von schränken (auch als "CAB-Dateien" bezeichnet). Außerdem bietet die Bibliothek Komprimierung, um die Größe der in den Schränken gespeicherten Datei Daten zu reduzieren.



| Funktion                                   | BESCHREIBUNG                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Datei "file"**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Fügt der CAB-Datei eine Datei hinzu.<br/>                                           |
| [**"F" erstellen**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Erstellt einen FCI-Kontext.<br/>                                                                          |
| [**Mit der Verschlüsselung**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Löscht einen geöffneten FCI-Kontext, wodurch alle dem Kontext zugeordneten Speicher-und temporären Dateien freigegeben werden.<br/> |
| [**"Sciflushcabinet"**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Schließt den aktuellen Schrank ab.<br/>                                                                   |
| [**Ordner "sciflushfolder"**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Erzwingt, dass der aktuelle Ordner in der Konstruktion sofort abgeschlossen wird.<br/>                        |



 

## <a name="fdi-functions"></a>FDI-Funktionen

Die Bibliothek "FDI (File decompression Interface)" bietet die Möglichkeit, Dateien aus schränken zu extrahieren.



| Funktion                                         | BESCHREIBUNG                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Nicht kopieren**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrahiert Dateien aus kabinatendateien.<br/>                                                          |
| [**"F" erstellen**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Erstellt einen FDI-Kontext.<br/>                                                                |
| [**Nicht löschen**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Löscht einen geöffneten FDI-Kontext.<br/>                                                           |
| [**"F"**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Bestimmt, ob eine Datei eine CAB-Datei ist, und gibt ggf. beschreibende Informationen zurück.<br/> |
| [**"F"**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Verkürzt eine CAB-Datei ab der angegebenen Ordner Nummer.<br/>                      |



 

## <a name="deprecated-functions"></a>Veraltete Funktionen

-   [**Deleteextractedfiles**](deleteextractedfiles.md)
-   [**Dllgetversion**](dllgetversion.md)
-   [**Extrahieren**](extract.md)
-   [**Getdllversion**](getdllversion.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CAB-API-Referenz](cabinet-api-reference.md)
</dt> <dt>

[Verwenden der CAB-API](using-the-cabinet-api.md)
</dt> </dl>

 

 




