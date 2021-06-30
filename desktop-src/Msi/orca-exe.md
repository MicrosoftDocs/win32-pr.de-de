---
description: Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten Windows Installer Paketen und Mergemodulen.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102159"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten Windows Installer Paketen und Mergemodulen. Das Tool stellt eine grafische Benutzeroberfläche für die Validierung bereit, die die bestimmten Einträge hervorhebt, in denen Validierungsfehler oder Warnungen auftreten.

Dieses Tool ist nur in der Windows SDK [Components for Windows Installer Developers verfügbar.](platform-sdk-components-for-windows-installer-developers.md) Sie wird als Orca.msi bereitgestellt. Doppelklicken Sie nach der Windows SDK Components for Windows Installer Developers auf Orca.msi, um die Orca.exe zu installieren.

## <a name="syntax"></a>Syntax

**orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Orca.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden.



| Option | Beschreibung                                                 |
|--------|-------------------------------------------------------------|
| -q     | Stiller Modus                                                  |
| -S     | <*Datenbank*> Schemadatenbank \[ "orca.dat" – Standard\] |
| -?     | Hilfedialogfeld                                                 |



 

Orca.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird, mit Mergemodulen. Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden. Beim Mergen sind die Quelldateidateien -f, -m und -m <*alle*> erforderlich.



| Option     | Beschreibung                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Führen Sie einen Commit für die Zusammenführung in die Datenbank aus, wenn keine Fehler auftreten.                                     |
| -!         | Führen Sie auch dann einen Commit für die Zusammenführung in eine Datenbank durch, wenn Fehler auftreten.                       |
| -M         | <*modul*> Merge Module to merge into database (Modul zum Zusammenführen mit der Datenbank).                      |
| -f         | \[Feature:Feature2-Funktionen \] zum Herstellen einer Verbindung mit dem Mergemodul.                |
| -r         | <*Verzeichnis-ID*> Verzeichniseintrag für die Stammumleitung des Moduls.    |
| -X         | <*Verzeichnis>* Dateien in ein Image unter dem Verzeichnis extrahieren.         |
| -g         | <*Language*> Sprache, die zum Öffnen eines Moduls verwendet wird.                         |
| -l         | <*Protokolldatei>* Datei, die als Protokoll verwendet werden soll, fügen Sie an, wenn sie bereits vorhanden ist.      |
| -i         | <*Verzeichnis>* Dateien in das Quellimage unter dem Verzeichnis extrahieren. |
| -cab       | <*Dateiname>* MsM-Schränkung in Datei extrahieren.                        |
| -lfn       | Verwenden Sie lange Dateinamen während der Extraktion.                                 |
| -configure | <*filename>* Konfigurieren sie das Modul mithilfe von Daten aus einer Datei.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



