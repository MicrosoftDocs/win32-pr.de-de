---
description: Die folgenden Setup-API-Funktionen werden für INF-Dateien verwendet.
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: Setup Funktionen für die INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362825"
---
# <a name="inf-file-setup-functions"></a>Setup Funktionen für die INF-Datei

Die folgenden Setup-API-Funktionen werden für INF-Dateien verwendet.



| Funktion                                                                         | BESCHREIBUNG                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Setupcloseinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | Gibt Ressourcen frei und schließt den INF-handle.                                                                                                                                                             |
| [**Setupdecompressorcopyfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | Kopiert eine Datei und dekomprimiert Sie, falls erforderlich.                                                                                                                                                      |
| [**Setupfindfirstline**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | Sucht die erste Zeile in einem Abschnitt einer INF-Datei oder, wenn ein Schlüssel angegeben ist, die erste Zeile, die mit diesem Schlüssel übereinstimmt. Sie aktualisiert den **linienmember** einer [**infcontext**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) -Struktur. |
| [**Setupfindnextline**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | Gibt die nächste Zeile in einem Abschnitt relativ zum **linienmember** der angegebenen [**infcontext**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) -Struktur zurück.                                                                    |
| [**Setupfindnextmatchline**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | Gibt die nächste Zeile in einem Abschnitt relativ zum **linienmember** des angegebenen [**infcontext**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) zurück, der einem angegebenen Schlüssel entspricht.                                                 |
| [**Setupgetbinaryfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | Ruft Daten aus einer Zeile ab, deren Felder das binäre Format aufweisen.                                                                                                                                          |
| [**Setupgetfieldcount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | Gibt die Anzahl der Felder in einer Zeile zurück.                                                                                                                                                                |
| [**Setupgetfilecompressioninfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | Ruft Datei Komprimierungs Informationen aus einer INF-Datei ab.                                                                                                                                               |
| [**Setupgetinffilelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | Ruft eine Liste der Typen von INF-Dateien in einem angegebenen Verzeichnis ab.                                                                                                                                        |
| [**Setupgetinfinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | Gibt Informationen zu einer INF-Datei zurück (als **Zeilen** Mitglied von [**infcontext**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) oder filename).                                                                                     |
| [**Setupgetintfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | Gibt das angegebene ganzzahlige Feld einer Zeile in einer INF-Datei zurück.                                                                                                                                          |
| [**Setupgetlinebyindex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | Aktualisiert das **linienmember** eines [**infcontext**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) für die Zeile an einem angegebenen Index im angegebenen Abschnitt.                                                                     |
| [**Setupgetlinecount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | Gibt die Anzahl der Zeilen im angegebenen Abschnitt zurück.                                                                                                                                                  |
| [**Setupgetlinetext**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | Ruft den Inhalt einer angegebenen Zeile aus einer INF-Datei ab.                                                                                                                                            |
| [**Setupgetmultiszfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | Gibt eine Liste von Zeichen folgen zurück, beginnend mit dem angegebenen Feld einer Zeile in einer INF-Datei.                                                                                                                   |
| [**Setupgetsourcefileloation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | Ruft die Ordnungszahl und den Pfad des Quell Datenträgers (relativ zum Quell Stamm) ab, wo sich die Quelldatei befindet.                                                                                                       |
| [**Setupgetsourcefilesize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | Ruft die Dateigröße für eine einzelne Quelldatei oder den Abschnitt zum **Kopieren von Dateien** einer INF-Datei ab.                                                                                                           |
| [**Setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | Ruft den Pfad, die Tagdatei oder die Beschreibung für eine Quelle ab.                                                                                                                                             |
| [**Setupgetstringfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | Gibt das angegebene Zeichen folgen Feld einer Zeile in einer INF-Datei zurück.                                                                                                                                           |
| [**Setupgettargetpath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | Ruft den Zielpfad für den Abschnitt zum **Kopieren von Dateien** in einer INF-Datei ab.                                                                                                                                      |
| [**Setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | Installiert eine Datei.                                                                                                                                                                                       |
| [**Setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | Installiert eine Datei und gibt eine Variable zurück, die angibt, ob die Datei verwendet wurde.                                                                                                                  |
| [**Setupinstallfilesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | Fügt alle in den Abschnitten **Dateien kopieren**, **Dateien löschen** und **Umbenennen** von Dateien angegebenen Dateien in die Warteschlange ein, die in einem **Installations** Abschnitt aufgelistet sind.                                                       |
| [**Setupinstallfrominf-Abschnitt**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | Führt die Anweisungen aus, die im Abschnitt zur **Installation** der INF-Datei angegeben sind.                                                                                                                                  |
| [**Setupinstallservicesfrominf-Abschnitt**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | Führt Dienst Installations-und Löschvorgänge wie in einem **Dienst** Abschnitt einer INF-Datei angegeben aus.                                                                                            |
| [**Setupopumappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | Öffnet eine INF-Datei und fügt Sie an ein vorhandenes INF-Handle an.                                                                                                                                             |
| [**Setupopuminffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | Öffnet eine INF-Datei und gibt ein Handle dafür zurück.                                                                                                                                                          |
| [**Setupopeinmasterinf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | Öffnet die INF-Datei, die Datei-und Layoutinformationen für Dateien enthält, die im System ausgeliefert werden.                                                                                                        |
| [**Setupqueryinffileinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | Fragt eine INF-Informationsstruktur über die zugeordneten INF-Dateinamen ab.                                                                                                                               |
| [**Setupqueryinfversioninformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | Fragt eine INF-Informationsstruktur nach Versionsinformationen für eine der zugehörigen INF-Dateien ab.                                                                                                      |
| [**Setupsetdirectoriyid**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | Ordnet einen neuen Verzeichnis Bezeichner einem bestimmten Verzeichnis zu.                                                                                                                                     |



 

 

 



