---
description: Um das Beispiel zu reproduzieren, das Sie kopieren oder mit einem Software Tool erstellen müssen, eine Windows Installer Datenbankdatei.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importieren einer leeren Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216938"
---
# <a name="importing-a-blank-database"></a>Importieren einer leeren Datenbank

Um das Beispiel zu reproduzieren, das Sie kopieren oder mit einem Software Tool erstellen müssen, eine Windows Installer Datenbankdatei. Eine vollständig leere Installations Datenbank, Schema.msi, wird mit den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Das SDK stellt außerdem eine teilweise leere Datenbank (uisample.msi) bereit, die die vorgeschlagenen Sequenz Tabellen und Daten enthält, die für eine einfache Benutzeroberfläche erforderlich sind. Erstellen Sie eine Kopie von uisample.msi, und verschieben Sie Sie in das Verzeichnis, in dem sich der Ordner befindet, den Sie unter [Planen der Installation](planning-the-installation.md)erstellt haben. Benennen Sie die Datei MNP2000.msi um. Die Installationsdaten Bank Datei und die Quelldateien müssen sich im Stammverzeichnis desselben Verzeichnisses befinden. Beispiel:

C: \\ Beispiel \\MNP2000.msi

C: \\ Beispiel für \\ Notepad\\

Wenn Sie Uisample.msi nicht verwenden, müssen Sie eine leere Datenbank (z. b. Schema.msi) abrufen und Informationen für die Installation mithilfe eines Tools zur Datenbankbearbeitung, wie z. b. Orca, das mit dem SDK bereitgestellt wird, oder eines anderen Daten Bank Editors eingeben.

[Fortsetzen](specifying-directory-structure.md)

 

 



