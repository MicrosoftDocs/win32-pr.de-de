---
description: Im Abschnitt Installieren einer INF-Datei werden die Schritte der Installationsprozedur definiert.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Beispiel für INF-Installations Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353619"
---
# <a name="inf-install-section-example"></a>Beispiel für INF-Installations Abschnitt

Im Abschnitt **Installieren** einer INF-Datei werden die Schritte der Installationsprozedur definiert. Jede Zeile eines **Installations** Abschnitts besteht aus zwei Teilen. Auf der linken Seite des Gleichheitszeichens (=) ist der Schlüssel. Auf der rechten Seite ist eine Liste mit mindestens einem Abschnitts Titel. Der Schlüssel gibt den Typ der Abschnitte an, die auf der rechten Seite aufgeführt sind. Eine Beschreibung des Formats dieses Abschnitts finden Sie in den Abschnitten und Direktiven der INF-Datei des Microsoft Windows 2000 Driver Development Kit.

Im folgenden finden Sie ein Beispiel für einen **Installations** Abschnitt.

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

In diesem Beispiel wird der **CopyFiles** -Schlüssel auf die Werte "DATAFILES" und "Program Files" festgelegt. Dies gibt zwei Abschnitte zum **Kopieren von Dateien** in der INF-Datei an, die die Namen der Quelldateien enthalten, die bei Kopier Vorgängen verwendet werden. Das Ziel für die kopierten Dateien wird in einem **DestinationDirs** -Abschnitt in der INF-Datei angegeben.

Der " **Delta files** "-Schlüssel erhält den Wert "oldfiles". Dies gibt den Abschnitt **Dateien löschen** an, der Informationen enthält, die für Datei Löschvorgänge relevant sind.

Der Schlüssel **UpdateInis** gibt die **Update-INI-Datei** Abschnitte an, die Informationen zum Aktualisieren von Einträgen in der INI-Datei enthalten.

Die Schlüssel " **adressg** " und " **DelReg** " geben Abschnitte " **Registrierung hinzufügen** " und " **Löschen** " an, die Informationen zum Hinzufügen oder Löschen von Registrierungs

 

 



