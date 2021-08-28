---
description: Befolgen Sie diese Richtlinien, um die Lokalisierung von Paketen Windows Installer zu vereinfachen.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Vorbereiten eines Windows Installerpakets für die Lokalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e9a1ce06e74197dc8844622861a1f42252deae8b96d3ce57ea852673818de3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129160"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Vorbereiten eines Windows Installerpakets für die Lokalisierung

Die Lokalisierung eines Windows Installer-Pakets in mehreren Sprachen kann durch Folgendes stark vereinfacht werden:

-   Erstellen Sie eine Basisinstallationsdatenbank, die codepageneutral ist. Weitere Informationen [finden Sie unter Erstellen einer Datenbank mit einer neutralen Codepage.](creating-a-database-with-a-neutral-code-page.md) Die Codepage der lokalisierten Datenbank kann dann durch Importieren einer Textarchivtabelle mit einer nicht neutralen Codepage in die Basisdatenbank festgelegt werden. Weitere [Informationen finden Sie unter Festlegen der Codepage einer Datenbank.](setting-the-code-page-of-a-database.md)
-   Organisieren Sie Dateien, die Lokalisierung erfordern, in separaten Komponenten, und installieren Sie diese Dateien in separaten Verzeichnissen. Dadurch wird sichergestellt, dass zwei lokalisierte Pakete niemals dateien mit identischen Namen im gleichen Verzeichnis installieren.

Beispielsweise kann eine weltweite Anwendung, die die folgenden Ressourcen verwendet, drei Komponenten haben.



| Komponente | Ressource                   |
|-----------|----------------------------|
| Welt     | worldwide.exe              |
| Welt     | weltweite Registrierungseinträge |
| Welt     | weltweite Verknüpfung         |
| DE       | engui.dll                  |
| DE       | ReadMe.txt                 |
| FRA       | fraui.dll                  |
| FRA       | ReadMe.txt                 |



 

Die dateien, die lokalisiert werden müssen, können an den folgenden Verzeichnispfaden installiert werden:

-   \[ProgramFilesFolder \] \\ World \\worldwide.exe
-   \[ProgramFilesFolder \] \\ World English \\ \\engui.dll
-   \[ProgramFilesFolder \] \\ World English \\ \\readme.txt
-   \[ProgramFilesFolder \] \\ World Französisch \\ \\fraui.dll
-   \[ProgramFilesFolder \] \\ World Französisch \\ \\readme.txt

 

 



