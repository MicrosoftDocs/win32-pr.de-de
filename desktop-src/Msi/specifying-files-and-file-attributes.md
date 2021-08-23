---
description: Die Installation und Entfernung jeder Datei wird durch die Windows Installer-Komponente bestimmt, die die Datei steuert.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Angeben von Dateien und Dateiattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdb63bf2779ddc5730013bad06b382c168a62bab5e897d5d621f7a65644e445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893730"
---
# <a name="specifying-files-and-file-attributes"></a>Angeben von Dateien und Dateiattributen

Die Installation und Entfernung jeder Datei wird durch die [Windows Installer-Komponente](windows-installer-components.md) bestimmt, die die Datei steuert. Nachdem die Gruppierung von Ressourcen in Komponenten angegeben wurde, können der Installationsdatenbank Dateiattributinformationen hinzugefügt werden. In diesem Abschnitt fügen Sie der Installationsdatenbank Dateiinformationen für das Editor Beispiel hinzu. Weitere Informationen finden Sie unter [Dateitabellengruppe.](file-tables-group.md)

Die Dateien im Editor Beispiel sind nicht komprimiert. Informationen zum Hinzufügen von Cab-Dateien zu Paketen finden Sie unter [Komprimierte und unkomprimierte Quellen.](compressed-and-uncompressed-sources.md) Dieses Beispiel enthält keine Informationen zur Dateiversionsversionsierung. Weitere Informationen zur Dateiversionsversionsierung finden Sie unter [Dateiversionsierungsregeln](file-versioning-rules.md) und [Standarddateiversionsierung.](default-file-versioning.md)

Verwenden Sie den Datenbank-Editor, um MNP2000.msi zu öffnen und die folgenden Daten in die leere Dateitabelle einzugeben.

[Dateitabelle](file-table.md)



| Datei         | Komponente\_ | FileName     | FileSize | Version | Sprache | Attribute | Sequenz |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Baseball    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Konzert     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Tanz       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Fußball    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Hilfe        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Editor     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Editor     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Fortsetzen](specifying-source-media.md)

 

 



