---
description: Die folgenden Funktionen werden mit den Metadateien des erweiterten Formats verwendet.
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: Metafile-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528316"
---
# <a name="metafile-functions"></a>Metafile-Funktionen

Die folgenden Funktionen werden mit den Metadateien des erweiterten Formats verwendet.



| Funktion                                                             | BESCHREIBUNG                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | Schließt einen erweiterten Metafile-Gerätekontext.                                                                            |
| [**Copyenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | Kopiert den Inhalt einer Metadatei mit erweitertem Format in eine angegebene Datei.                                                |
| [**"Kreateenhmetafile"**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | Erstellt einen Gerätekontext für eine Metadatei mit erweitertem Format.                                                              |
| [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | Löscht eine-Metadatei im erweiterten Format oder ein-metadateihandle mit erweitertem Format.                                             |
| [**Enhmetafileproc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | Eine von der Anwendung definierte Rückruffunktion, die mit der enumenhmetafile-Funktion verwendet wird.                                       |
| [**Enumenhyfile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | Listet die Datensätze in einer Metadatei mit erweitertem Format auf.                                                             |
| [**Gdicomment**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | Kopiert einen Kommentar aus einem Puffer in eine angegebene Metadatendatei mit erweitertem Format.                                              |
| [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | Erstellt ein Handle, das die in der angegebenen Datei gespeicherte Metadatei mit erweitertem Format identifiziert.                            |
| [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | Ruft den Inhalt der angegebenen Metadatei mit erweitertem Format ab und kopiert sie in einen Puffer.                        |
| [**Getenhmetafiledescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | Ruft eine optionale Textbeschreibung aus einer Metadatei mit erweitertem Format ab und kopiert die Zeichenfolge in den angegebenen Puffer. |
| [**Getenhmetafileheader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | Ruft den Datensatz mit dem-Header für die angegebene Metadatei mit erweitertem Format ab.                                 |
| [**Getenhmetafilepaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | Ruft optionale Paletteneinträge aus der angegebenen erweiterten Metadatei ab.                                               |
| [**Getmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | Getmetafile ist nicht mehr für die Verwendung ab Windows 2000 verfügbar. Verwenden Sie stattdessen [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea).  |
| [**Getwinmetafilebits**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | Konvertiert die Datensätze mit erweitertem Format aus einer Metadatei in Datensätze im Windows-Format.                                      |
| [**Playenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | Zeigt das Bild an, das in der angegebenen Metadatei mit erweitertem Format gespeichert ist.                                                 |
| [**Playenhmetafilerecord**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | Gibt einen erweiterten Metadateidatensatz wieder, indem die vom Datensatz identifizierten Funktionen der Graphics Device Interface (GDI) ausgeführt werden. |
| [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | Erstellt aus den angegebenen Daten eine speicherbasierte Metadatei mit erweitertem Format.                                               |
| [**Setwinmetafilebits**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | Konvertiert eine Metadatei aus dem älteren Windows-Format in das neue erweiterte Format.                                          |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen sind veraltet. Die werden aus Gründen der Kompatibilität mit Metadateien im Windows-Format bereitgestellt.

-   [**Closemetafile**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**Copymetafile**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**"Kreatemetafile"**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**DeleteMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**Enummetadatei**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**Enummetafileproc**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**GetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**Playmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**Playmetafilerecord**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**SetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
