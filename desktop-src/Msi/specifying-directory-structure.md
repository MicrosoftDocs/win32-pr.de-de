---
description: Der Installer speichert Informationen zur Installationsverzeichnis Struktur in der Verzeichnis Tabelle.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Angeben der Verzeichnisstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862908"
---
# <a name="specifying-directory-structure"></a>Angeben der Verzeichnisstruktur

Der Installer speichert Informationen zur Installationsverzeichnis Struktur in der [Verzeichnis Tabelle](directory-table.md). Weitere Informationen finden Sie in der [Gruppe der Kern Tabellen](core-tables-group.md) In diesem Abschnitt fügen Sie der leeren Datenbank, die Sie unter [Importieren einer leeren Datenbank](importing-a-blank-database.md)erstellt haben, Verzeichnisstruktur Informationen für das Notepad-Beispiel hinzu. Verwenden Sie den Datenbank-Editor, der mit dem SDK bereitgestellt wird, oder einen anderen Editor, um die Verzeichnis Tabelle in MNP2000.msi zu öffnen. Verwenden Sie den Editor, um die folgenden Daten in die leere Verzeichnis Tabelle einzugeben.

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis                                        | Über \_ geordnetes Verzeichnis                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| Argsdir                                          | Notepaddir                                       | Kunst: Ereignisse       |
| Holdir                                           | Mondir                                           | .: Feiertage        |
| Menudir                                          | Notepaddir                                       | Menü              |
| Mondir                                           | Notepaddir                                       | Tors              |
| Notepaddir                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Roter \_ Park: Notepad |
| Sportdir                                         | Notepaddir                                       | Sport: Ereignisse     |



 

Wenn Sie diese Daten in die Verzeichnis Tabelle eingeben, werden die Quell-und Zielverzeichnis Strukturen angegeben. Informationen finden Sie in der [Verzeichnis Tabelle](directory-table.md) und in den Themen zu [den Verzeichnis Tabellen](using-the-directory-table.md) . Beachten Sie, dass es sich bei der [**TARGETDIR**](targetdir.md) -Eigenschaft um den Namen eines Stamms in der Verzeichnis Tabelle jeder Installation handeln muss.

[Fortsetzen](specifying-components.md)

 

 



