---
title: Projfs-Funktionen
description: Die folgenden Funktionen werden in projectedfslib. h deklariert.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 40f3f2aec8e52d2caafdcf1554d0871e9bb185de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337702"
---
# <a name="projfs-functions"></a>Projfs-Funktionen

Die folgenden Funktionen werden in projectedfslib. h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**Prjzuzuordnen catealignedbuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Ordnet einen Puffer zu, der die Anforderungen für die Speicher Ausrichtung des Speichergeräts der virtualisierungsinstanz erfüllt. |
| [**Prjclearnegativepathcache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Löscht den negativen Pfad Cache der virtualisierungsinstanz, wenn er aktiv ist. |
| [**Prjcompletecommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Gibt an, dass der Anbieter die Verarbeitung eines Rückrufs abgeschlossen hat, von dem er zuvor HRESULT_FROM_WIN32 (ERROR_IO_PENDING) zurückgegeben hat. |
| [**Prjdeletefile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Ermöglicht einem Anbieter das Löschen eines Elements, das auf dem lokalen Dateisystem zwischengespeichert wurde. |
| [**Prjdoesnamecontainwildcards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Bestimmt, ob ein Name Platzhalter Zeichen enthält. |
| [**Prjdateinamecompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Vergleicht zwei Dateinamen und gibt einen Wert zurück, der die relative Sortierreihenfolge angibt. |
| [**Prjfile-amematch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Bestimmt, ob ein Dateiname mit einem Suchmuster übereinstimmt. |
| [**Prjfilldirentrybuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Stellt Informationen für eine Datei oder ein Verzeichnis für eine Enumeration bereit. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Stellt Informationen für eine Datei oder ein Verzeichnis für eine Enumeration bereit und ermöglicht es dem Aufrufer, erweiterte Informationen anzugeben. |
| [**Prjfrealignedbuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Gibt einen zugeordneten Puffer frei. |
| [**Prjgetondiskfilestate**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Ruft den Datei Zustand auf dem Datenträger für eine Datei oder ein Verzeichnis ab. |
| [**Prjgetvirtualizationinstanceingefo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Ruft Informationen zur virtualisierungsinstanz ab. |
| [**Prjmarkdirector yasplachalter**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Konvertiert ein vorhandenes Verzeichnis in einen Verzeichnis Platzhalter. |
| [**Prjstartvirtualisieren**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Konfiguriert eine projfs-virtualisierungsinstanz und startet Sie, sodass Sie für die Dienst-e/a verfügbar ist und Rückrufe für den Anbieter aufgerufen wird. |
| [**Prjstopvirtualisieren**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Beendet eine laufende projfs-virtualisierungsinstanz, sodass Sie für die Dienst-e/a nicht verfügbar ist oder Rückrufe für den Anbieter einschließt. |
| [**Prjupdatefileifbenötigter**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Ermöglicht einem Anbieter, ein Element zu aktualisieren, das auf dem lokalen Dateisystem zwischengespeichert wurde. |
| [**Prjschreitefiledata**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Sendet Dateiinhalte an projfs. |
| [**Prjschreiteplaceholderinfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Sendet Datei-oder Verzeichnis Metadaten an projfs. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Sendet Datei-oder Verzeichnis Metadaten an projfs und ermöglicht dem Aufrufer, erweiterte Informationen anzugeben. |
