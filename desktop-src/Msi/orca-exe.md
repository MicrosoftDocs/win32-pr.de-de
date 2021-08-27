---
description: Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer-Paketen und Mergemodulen.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f1b0d31936bf81e60efd8eb9799ddb30b4d5a6f78363e2ff5d3d638ae40c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082680"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer-Paketen und Mergemodulen. Das Tool stellt eine grafische Oberfläche für die Überprüfung bereit, die die einträge hervorhebt, in denen Validierungsfehler oder Warnungen auftreten.

Dieses Tool ist nur in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar. Sie wird als Orca.msi Datei bereitgestellt. Doppelklicken Sie nach der Installation der Windows SDK-Komponenten für Windows Installer-Entwickler auf Orca.msi, um die Orca.exe-Datei zu installieren.

## <a name="syntax"></a>Syntax

**orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Orca.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Anstelle eines Bindestrichs kann auch ein Schrägstrichtrennzeichen verwendet werden.



| Option | BESCHREIBUNG                                                 |
|--------|-------------------------------------------------------------|
| -q     | Stiller Modus                                                  |
| -S     | <*datenbank*> Schemadatenbank \[ "orca.dat" – Standard\] |
| -?     | Hilfedialogfeld                                                 |



 

Orca.exe verwendet die folgenden Befehlszeilenoptionen ohne Beachtung der Groß-/Kleinschreibung mit Mergemodulen. Anstelle eines Bindestrichs kann auch ein Schrägstrichtrennzeichen verwendet werden. Beim Ausführen eines Merges sind die> -f, -m und <*Quelldatei* erforderlich.



| Option     | Beschreibung                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Führen Sie einen Commit für die Zusammenführung in die Datenbank aus, wenn keine Fehler auftreten.                                     |
| -!         | Führen Sie einen Commit für die Zusammenführung in eine Datenbank aus, auch wenn Fehler vorliegen.                       |
| -M         | <*-Modul*> Merge-Moduls zum Zusammenführen in die Datenbank.                      |
| -f         | \[Feature:Feature2-Features zum Herstellen einer \] Verbindung mit dem Mergemodul.                |
| -r         | <*Verzeichnis-ID*> Verzeichniseintrag für die Stammumleitung des Moduls.    |
| -X         | <*Verzeichnis*> Extrahieren von Dateien in ein Image unter dem Verzeichnis.         |
| -g         | <*Language*> Sprache, die zum Öffnen eines Moduls verwendet wird.                         |
| -l         | <*Protokolldatei*> Datei, die als Protokoll verwendet werden soll, anfügen, wenn sie bereits vorhanden ist.      |
| -i         | <*directory*> Extrahieren von Dateien in das Quellimage unter dem Verzeichnis. |
| -cab       | <*Dateiname*> Extrahieren des MSM-Schränks in eine Datei.                        |
| -lfn       | Verwenden Sie lange Dateinamen während der Extraktion.                                 |
| -configure | <*dateiname*> Konfigurieren des Moduls mithilfe von Daten aus einer Datei.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installationsentwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



