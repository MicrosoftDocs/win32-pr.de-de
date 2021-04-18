---
description: Die Installation und das Entfernen der einzelnen Dateien werden durch die Windows Installer Komponente bestimmt, die die Datei steuert.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Angeben von Dateien und Dateiattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347535"
---
# <a name="specifying-files-and-file-attributes"></a>Angeben von Dateien und Dateiattributen

Die Installation und das Entfernen der einzelnen Dateien werden durch die [Windows Installer Komponente](windows-installer-components.md) bestimmt, die die Datei steuert. Nachdem die Gruppierung von Ressourcen in Komponenten angegeben wurde, können der Installations Datenbank Datei Attributinformationen hinzugefügt werden. In diesem Abschnitt fügen Sie der-Installations Datenbank Dateiinformationen für das Notepad-Beispiel hinzu. Weitere Informationen finden Sie in der [Gruppe Datei Tabellen](file-tables-group.md).

Die Dateien im Notepad-Beispiel sind nicht komprimiert. Informationen zum Hinzufügen von CAB-Dateien zu Paketen finden Sie unter [komprimierte und nicht komprimierte Quellen](compressed-and-uncompressed-sources.md) . Dieses Beispiel enthält keine Informationen zur Datei Versionsverwaltung. Weitere Informationen zur Datei Versionsverwaltung finden Sie unter [Regeln für die Datei Versions](file-versioning-rules.md) Verwaltung und [standardmäßige Datei Versions](default-file-versioning.md)Verwaltung.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere Dateitabelle ein.

[Dateitabelle](file-table.md)



| File         | Komponente\_ | FileName     | FileSize | Version | Sprache | Attribute | Sequenz |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Ball    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Konzert     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Abhängigkeit       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Verbandes    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Hilfe        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | Newyears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Editor     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Editor     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Fortsetzen](specifying-source-media.md)

 

 



