---
description: Befolgen Sie diese Richtlinien, um die Lokalisierung von Windows Installer Paketen zu vereinfachen.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Vorbereiten eines Windows Installer Pakets für die Lokalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344242"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Vorbereiten eines Windows Installer Pakets für die Lokalisierung

Die Lokalisierung eines Windows Installer Pakets in mehrere Sprachen kann durch folgende Aktionen deutlich vereinfacht werden:

-   Erstellen Sie eine Basis-Installations Datenbank, die Code Page neutral ist. Weitere Informationen finden Sie [unter Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md). Die Codepage der lokalisierten Datenbank kann dann festgelegt werden, indem eine Textarchiv Tabelle mit einer nicht neutralen Codepage in die Basisdatenbank importiert wird. Siehe [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).
-   Organisieren Sie Dateien, die eine Lokalisierung in separate Komponenten erfordern, und installieren Sie diese Dateien in separaten Verzeichnissen. Dadurch wird sichergestellt, dass zwei lokalisierte Pakete niemals Dateien mit identischem Namen im selben Verzeichnis installieren.

Beispielsweise kann eine weltweite Anwendung, die die folgenden Ressourcen verwendet, drei Komponenten aufweisen.



| Komponente | Resource                   |
|-----------|----------------------------|
| World     | worldwide.exe              |
| World     | weltweite Registrierungseinträge |
| World     | weltweite Verknüpfung         |
| DE       | engui.dll                  |
| DE       | ReadMe.txt                 |
| FRA       | fraui.dll                  |
| FRA       | ReadMe.txt                 |



 

Die Dateien, die lokalisiert werden müssen, können in den folgenden Verzeichnis Speicherorten installiert werden:

-   \[ProgramFilesFolder \] \\ World \\worldwide.exe
-   \[ProgramFilesFolder \] \\ World \\ English \\engui.dll
-   \[ProgramFilesFolder \] \\ World \\ English \\readme.txt
-   \[ProgramFilesFolder \] \\ World \\ French \\fraui.dll
-   \[ProgramFilesFolder \] \\ World \\ French \\readme.txt

 

 



