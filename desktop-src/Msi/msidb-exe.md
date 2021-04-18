---
description: Msidb.exe verwendet msidatabaseimport und msidatabaseexport, um Datenbanktabellen und Streams zu importieren und zu exportieren.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351747"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe verwendet [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) und [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) , um [Datenbanktabellen](database-tables.md) und Streams zu importieren und zu exportieren.

Wenn der Modus, der Ordner, die Datenbank und die Tabelle in der Befehlszeile angegeben sind, wird Msidb.exe keine Benutzeroberfläche angezeigt und fungiert als automatisches Befehlszeilen-Hilfsprogramm, das für das Buildskript geeignet ist.

## <a name="syntax"></a>Syntax

**Msidb** *{Option} ***..** . _{Option}_* _..._ * * {Table} ***..** . _{Table}_

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msidb.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importieren Sie Textarchiv Dateien aus dem Ordner in die-Datenbank. Tabellennamen für den Import sind Dateinamen, die 8 Zeichen lang sind, mit der Erweiterung ". IDT". Längere Namen werden auf 8 Zeichen gekürzt, wenn Sie vom Befehl für den Import bereitgestellt werden. Es können Standard mäßige Platzhalter Spezifikationen verwendet werden.                                                                 |
| -E     | Exportieren ausgewählter Tabellen aus einer Datenbank in Textarchiv Dateien im Ordner. Tabellennamen für den Export sind Tabellennamen. Es kann nur die Platzhalter Spezifikation " \* " verwendet werden. Tabellen können aus einer schreibgeschützten Datenbank exportiert werden.                                                                                                               |
| -c     | Erstellt eine neue Datenbankdatei und importiert Tabellen. Überschreibt eine vorhandene Datenbankdatei.                                                                                                                                                                                                                                               |
| -f     | Gibt den Ordner an, der die Textarchiv Dateien für Tabellen und Datenströme enthält. Wenn der Ordner, der die Textarchiv Dateien enthält, nicht angegeben ist, wird der Benutzer vom Hilfsprogramm zum Ordner aufgefordert.                                                                                                                                       |
| -d     | Voll qualifizierter Pfad zur Datenbankdatei.                                                                                                                                                                                                                                                                                          |
| -M     | Voll qualifizierter Pfad zur Datenbank, die in zusammengeführt werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen. Wenn die Datenbank nicht in der Befehlszeile angegeben ist, fordert das Hilfsprogramm den Benutzer zur Eingabe der Datenbank auf.                                       |
| -t     | Der voll qualifizierte Pfad der anzuwendenden Transformation. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                     |
| -j     | Der Name des Speichers, der aus der Datenbank entfernt werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                             |
| -k     | Der Name des Datenstroms, der aus der Datenbank entfernt werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                                 |
| -X     | Der Name des Datenstroms, der in einer Datenträger Datei im aktuellen Verzeichnis gespeichert werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Binäre Datenströme werden als separate Dateien mit der Erweiterung ". ibd" gespeichert. Der binäre Dateiname wird als Primärschlüssel Daten für die Zeile verwendet, die den Stream enthält.                                                  |
| -w     | Der Name des Speichers, der in einer Datenträger Datei im aktuellen Verzeichnis gespeichert werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar.                                                                                                                                                                                                         |
| -a     | Der Name der Datei, die der Datenbank als Stream hinzugefügt werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen. Binäre Datenströme werden als separate Dateien mit der Erweiterung ". ibd" gespeichert. Der binäre Dateiname wird als Primärschlüssel Daten für die Zeile verwendet, die den Stream enthält. |
| -r     | Der Name des Speichers, der der Datenbank als unter Speicher hinzugefügt werden soll. Diese Option ist nur im stillen Befehlszeilen Modus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                     |
| -S     | Kürzen Sie die Tabellennamen beim Exportieren in eine IDT-Tabelle auf 8 Zeichen. Der Tabellenname wird auf 8 Zeichen gekürzt, und die Erweiterung ". IDT" wird hinzugefügt.                                                                                                                                                                                           |
| -?     | Zeigt das Hilfe Dialogfeld der Befehlszeile an                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Wenn Sie lange Dateinamen mit Leerzeichen verwenden, verwenden Sie Anführungszeichen. Geben Sie beispielsweise für eine Datenbank, die sich im Ordner "eigene Dateien" befindet, den Wert "c: \\ Eigene Dokumente" an.

 

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



