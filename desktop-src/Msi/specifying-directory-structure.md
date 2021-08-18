---
description: Das Installationsprogramm speichert Informationen zur Installationsverzeichnisstruktur in der Verzeichnistabelle.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Angeben der Verzeichnisstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc71e448c03a7fdbdf9de249122246aaf0038769a1dd409551330a503be7e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627890"
---
# <a name="specifying-directory-structure"></a>Angeben der Verzeichnisstruktur

Das Installationsprogramm speichert Informationen zur Installationsverzeichnisstruktur in der [Verzeichnistabelle](directory-table.md). Weitere Informationen finden Sie [in der Gruppe "Kerntabellen".](core-tables-group.md) In diesem Abschnitt fügen Sie Der leeren Datenbank, die Sie in Importieren einer leeren Datenbank erstellt haben, Verzeichnisstrukturinformationen für das Beispiel Editor [hinzu.](importing-a-blank-database.md) Verwenden Sie den Datenbank-Editor Orca, der mit dem SDK bereitgestellt wird, oder einen anderen Editor, um die Verzeichnistabelle im MNP2000.msi. Geben Sie mithilfe des Editors die folgenden Daten in die leere Tabelle Directory ein.

[Verzeichnistabelle](directory-table.md)



| Verzeichnis                                        | Übergeordnetes \_ Verzeichnis                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**Targetdir**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**Targetdir**](targetdir.md)                   | .                 |
| MEMODIR                                          | NOTEPADDIR                                       | Schrift: Events       |
| HOLDIR                                           | MONDIR                                           | .:Festtage        |
| MENUDIR                                          | NOTEPADDIR                                       | Menü              |
| MONDIR                                           | NOTEPADDIR                                       | Gate              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park:Editor |
| SPORTDIR                                         | NOTEPADDIR                                       | Sport:Events     |



 

Wenn Sie diese Daten in die Directory-Tabelle eingeben, werden die Quell- und Zielverzeichnisstrukturen angegeben. Weitere Informationen finden [Sie in den Themen](directory-table.md) Verzeichnistabelle und Verwenden der [Verzeichnistabelle.](using-the-directory-table.md) Beachten Sie, [**dass die TARGETDIR-Eigenschaft**](targetdir.md) der Name eines Stamms in der Verzeichnistabelle jeder Installation sein muss.

[Fortsetzen](specifying-components.md)

 

 



