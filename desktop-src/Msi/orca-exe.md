---
description: Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer Paketen und Mergemodulen.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041674"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer Paketen und Mergemodulen. Das Tool stellt eine grafische Benutzeroberfläche für die Validierung bereit und hebt die einzelnen Einträge hervor, bei denen Validierungs Fehler oder Warnungen auftreten.

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar. Sie wird als Orca.msi Datei bereitgestellt. Nachdem Sie die Windows SDK Komponenten für Windows Installer Entwickler installiert haben, doppelklicken Sie auf Orca.msi, um die Orca.exe-Datei zu installieren.

## <a name="syntax"></a>Syntax

**Orca***\[<options>\]\[<source file>\]*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Orca.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.



| Option | BESCHREIBUNG                                                 |
|--------|-------------------------------------------------------------|
| -q     | Stiller Modus                                                  |
| -S     | <*Datenbank* -> Schema \[ -Datenbank "Orca. dat"-Default\] |
| -?     | Hilfe Dialogfeld                                                 |



 

Orca.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung mit Mergemodulen. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden. Beim Ausführen einer Zusammenführung sind alle> der Datei "-f", "-m" und "<*SourceFile* " erforderlich.



| Option     | Beschreibung                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Commit in Datenbank zusammenführen, wenn keine Fehler auftreten.                                     |
| -!         | Commit in eine Datenbank zusammenführen, auch wenn Fehler auftreten.                       |
| -M         | <*Modul*> Mergemodul zum Zusammenführen in die Datenbank.                      |
| -f         | Feature \[ : Feature2 \] Feature (e) zum Herstellen einer Verbindung mit dem Mergemodul.                |
| -r         | <*Verzeichnis-ID*> Verzeichniseintrag für die Modul Stamm Umleitung.    |
| -X         | <*Verzeichnis*> Dateien in ein Bild unter dem Verzeichnis extrahieren.         |
| -g         | <*Sprache*> Sprache, mit der ein Modul geöffnet wird.                         |
| -l         | <*Protokolldatei*> Datei, die als Protokoll verwendet werden soll, fügen Sie an, wenn Sie bereits vorhanden ist.      |
| -i         | <*Verzeichnis*> Dateien in das Quell Abbild im Verzeichnis extrahieren. |
| -CAB       | <*Dateiname*> den MSM-CAB in eine Datei extrahieren.                        |
| -LFN       | Verwenden Sie lange Dateinamen während der Extraktion.                                 |
| -Konfigurieren | <*Dateiname*> konfigurieren Sie das Modul mithilfe von Daten aus einer Datei.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



