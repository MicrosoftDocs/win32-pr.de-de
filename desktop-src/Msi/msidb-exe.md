---
description: Msidb.exe verwendet MsiDatabaseImport und MsiDatabaseExport, um Datenbanktabellen und -streams zu importieren und zu exportieren.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bff646ae3e933be5dbe37a774b72c10a0183fe9c793305292c9a11c4f417be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012929"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe verwendet [**MsiDatabaseImport und**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) [**MsiDatabaseExport,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) um Datenbanktabellen und [-streams zu](database-tables.md) importieren und zu exportieren.

Wenn der Modus, der Ordner, die Datenbank und die Tabellenliste in der Befehlszeile angegeben sind, wird von Msidb.exe keine Benutzeroberfläche angezeigt und als automatisches Befehlszeilenprogramm verwendet, das für das Buildskript geeignet ist.

## <a name="syntax"></a>Syntax

**MsiDb** *{Option}***...** _{option}_* _..._ * *{tabelle}***...** _{table}_

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msidb.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden.



| Option | Beschreibung                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importieren Sie Textarchivdateien aus dem Ordner in die Datenbank. Tabellennamen für den Import sind 8 Zeichen lange Dateinamen mit der Erweiterung ".idt". Längere Namen werden auf 8 Zeichen gekürzt, wenn sie vom Befehl für den Import angegeben werden. Es können Standard-Platzhalterspezifikationen verwendet werden.                                                                 |
| -E     | Exportieren Sie ausgewählte Tabellen aus der Datenbank in Textdateien im Ordner . Tabellennamen für den Export sind Tabellennamen. Es kann nur die Platzhalterspezifikation " \* " verwendet werden. Tabellen können aus einer schreibgeschützten Datenbank exportiert werden.                                                                                                               |
| -c     | Erstellt eine neue Datenbankdatei und importiert Tabellen. Überschreibt eine vorhandene Datenbankdatei.                                                                                                                                                                                                                                               |
| -f     | Gibt den Ordner an, der die Textarchivdateien für Tabellen und Streams enthält. Wenn der Ordner, der die Textarchivdateien enthält, nicht angegeben ist, fordert das Hilfsprogramm den Benutzer zur Eingabe des Ordners auf.                                                                                                                                       |
| -d     | Vollqualifizierter Pfad zur Datenbankdatei.                                                                                                                                                                                                                                                                                          |
| -M     | Vollqualifizierter Pfad zur Datenbank, in der zusammengeführt werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen. Wenn die Datenbank nicht in der Befehlszeile angegeben ist, fordert das Hilfsprogramm den Benutzer zur Eingabe der Datenbank auf.                                       |
| -t     | Vollqualifizierter Pfad zur anzuwendenden Transformation. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                     |
| -j     | Name des Speichers, der aus der Datenbank entfernt werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                             |
| -k     | Name des Streams, der aus der Datenbank entfernt werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                                 |
| -X     | Name des Streams, der in einer Datenträgerdatei im aktuellen Verzeichnis gespeichert werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Binäre Datenströme werden als separate Dateien mit der Erweiterung ".ibd" gespeichert. Der verwendete Binärdateiname ist primärer Schlüsseldaten für die Zeile, die den Stream enthält.                                                  |
| -w     | Der Name des Speichers, der in einer Datenträgerdatei im aktuellen Verzeichnis gespeichert werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar.                                                                                                                                                                                                         |
| -a     | Name der Datei, die der Datenbank als Stream hinzugefügt werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen. Binäre Datenströme werden als separate Dateien mit der Erweiterung ".ibd" gespeichert. Der verwendete Binärdateiname ist primärer Schlüsseldaten für die Zeile, die den Stream enthält. |
| -r     | Name des Speichers, der der Datenbank als Unterspeicher hinzugefügt werden soll. Diese Option ist nur im unbesendigten Befehlszeilenmodus verfügbar. Mehrere Instanzen dieser Option können maximal 10 vorkommen.                                                                                                                                                     |
| -S     | Schneidet Tabellennamen beim Export in eine IDT-Datei auf 8 Zeichen ab. Der Tabellenname wird auf 8 Zeichen gekürzt, und die Erweiterung ".idt" wird hinzugefügt.                                                                                                                                                                                           |
| -?     | Zeigt das Befehlszeilen-Hilfedialogfeld an.                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Wenn Sie lange Dateinamen mit Leerzeichen verwenden, verwenden Sie anführungszeichen. Geben Sie für eine Datenbank, die sich im Ordner "Eigene Dokumente" befindet, als "c: \\ meine Dokumente" an.

 

Dieses Tool ist nur in Windows [SDK-Komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Verteilbare Versionen](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



