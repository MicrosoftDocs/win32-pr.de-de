---
title: ProjFS-Funktionen
description: Die folgenden Funktionen werden in projectedfslib.h deklariert.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 47e4371a7d00ca6564223f7415a69ee0308bf8757041b49f5df9f214e6c978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792607"
---
# <a name="projfs-functions"></a>ProjFS-Funktionen

Die folgenden Funktionen werden in projectedfslib.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Ordnet einen Puffer zu, der die Speicherausrichtungsanforderungen des Speichergeräts der Virtualisierungsinstanz erfüllt. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Löschen des negativen Pfadcaches der Virtualisierungsinstanz, wenn er aktiv ist. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Gibt an, dass der Anbieter die Verarbeitung eines Rückrufs abgeschlossen hat, von dem er zuvor HRESULT_FROM_WIN32(ERROR_IO_PENDING). |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Ermöglicht einem Anbieter das Löschen eines Elements, das im lokalen Dateisystem zwischengespeichert wurde. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Bestimmt, ob ein Name Platzhalterzeichen enthält. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Vergleicht zwei Dateinamen und gibt einen Wert zurück, der ihre relative Sortierungsreihen reihenfolge angibt. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Bestimmt, ob ein Dateiname einem Suchmuster entspricht. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Stellt Informationen für eine Datei oder ein Verzeichnis für eine Enumeration zur Verfügung. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Stellt Informationen für eine Datei oder ein Verzeichnis für eine Enumeration zur Verfügung und ermöglicht es dem Aufrufer, erweiterte Informationen anzugeben. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Gibt einen zugeordneten Puffer frei. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Ruft den Dateistatus auf dem Datenträger für eine Datei oder ein Verzeichnis ab. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Ruft Informationen zur Virtualisierungsinstanz ab. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Konvertiert ein vorhandenes Verzeichnis in einen Verzeichnisplatzhalter. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Konfiguriert eine ProjFS-Virtualisierungsinstanz und startet sie, macht sie für Dienst-E/A verfügbar und ruft Rückrufe für den Anbieter auf. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Beendet eine ausgeführte ProjFS-Virtualisierungsinstanz, wodurch sie für Die Dienst-E/A nicht verfügbar ist oder Rückrufe für den Anbieter beinhaltet. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Ermöglicht einem Anbieter das Aktualisieren eines Elements, das im lokalen Dateisystem zwischengespeichert wurde. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Sendet Dateiinhalte an ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Sendet Datei- oder Verzeichnismetadaten an ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Sendet Datei- oder Verzeichnismetadaten an ProjFS und ermöglicht es dem Aufrufer, erweiterte Informationen anzugeben. |
