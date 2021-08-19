---
description: Um das Beispiel zu reproduzieren, müssen Sie eine Installationsdatenbankdatei kopieren oder mit einem Softwaretool Windows erstellen.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importieren einer leeren Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3d2c0a7b0fa8d6364a9eef66b830f94e3523c2dfece9c6e1ec459d146ace11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946597"
---
# <a name="importing-a-blank-database"></a>Importieren einer leeren Datenbank

Um das Beispiel zu reproduzieren, müssen Sie eine Installationsdatenbankdatei kopieren oder mit einem Softwaretool Windows erstellen. Eine vollständig leere Installationsdatenbank, Schema.msi, wird mit den Windows SDK-Komponenten für Windows [Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Das SDK stellt auch eine teilweise leere Datenbank bereit, uisample.msi, die die vorgeschlagenen Sequenztabellen und Daten enthält, die für eine einfache Benutzeroberfläche erforderlich sind. Erstellen Sie eine Kopie uisample.msi, und verschieben Sie sie in dasselbe Verzeichnis, das den ordner Editor enthält, den Sie in [Planning the Installation erstellt haben.](planning-the-installation.md) Benennen Sie die Datei MNP2000.msi. Die Installationsdatenbankdatei und die Quelldateien müssen sich beide im Stammverzeichnis desselben Verzeichnisses befinden. Beispiel:

C: \\ \\ BeispielMNP2000.msi

C: \\ \\ Beispiel Editor\\

Wenn Sie Uisample.msi nicht verwenden, müssen Sie eine leere Datenbank wie Schema.msi abrufen und Informationen für die Installation eingeben, indem Sie ein Datenbankbearbeitungstool wie Orca verwenden, das mit dem SDK bereitgestellt wird, oder einen anderen Datenbank-Editor.

[Fortsetzen](specifying-directory-structure.md)

 

 



