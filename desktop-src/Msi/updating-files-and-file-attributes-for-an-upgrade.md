---
description: Da beim Upgrade die von der Anwendung verwendeten Dateien aktualisiert werden, müssen Sie die Dateitabelle der Datenbank ändern.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Aktualisieren von Dateien und Dateiattributen für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c1d749a61376d38e8c7793ba5766dd63133bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354239"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Aktualisieren von Dateien und Dateiattributen für ein Upgrade

Da beim Upgrade die von der Anwendung verwendeten Dateien aktualisiert werden, müssen Sie die [Dateitabelle](file-table.md) der Datenbank ändern. Verwenden Sie den Datenbank-Editor, der mit dem SDK bereitgestellt wird, oder einen anderen Editor, um MNP2001.msi zu öffnen, und geben Sie die folgenden Daten in die [Dateitabelle](file-table.md)ein.

[Dateitabelle](file-table.md)



| File         | Komponente\_ | FileName     | FileSize | Version | Sprache | Attribute | Sequenz |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Ball    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | Konzert     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | Abhängigkeit       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | Verbandes    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | Erinnen  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Hilfe        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | January     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | Newyears    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | Denkmals    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Editor     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Editor     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Fortsetzen](updating-components-for-an-upgrade.md)

 

 



