---
description: Da beim Upgrade die von der Anwendung verwendeten Dateien aktualisiert werden, müssen Sie die Dateitabelle der Datenbank ändern.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Aktualisieren von Dateien und Dateiattributen für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c56560432a18746b31e3bb983be1f465199c51b15601c3dfd47911fe7f6ab4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809890"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Aktualisieren von Dateien und Dateiattributen für ein Upgrade

Da beim Upgrade die von der Anwendung verwendeten Dateien aktualisiert werden, müssen Sie die [Dateitabelle](file-table.md) der Datenbank ändern. Verwenden Sie den mit dem SDK bereitgestellten Datenbank-Editor Orca oder einen anderen Editor, um MNP2001.msi zu öffnen und die folgenden Daten in die [Dateitabelle](file-table.md)einzugeben.

[Dateitabelle](file-table.md)



| Datei         | Komponente\_ | FileName     | FileSize | Version | Sprache | Attribute | Sequenz |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Baseball    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | Konzert     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | Tanz       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | Fußball    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | Basketball  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Hilfe        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | January     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | NewYears    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | Memorial    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Editor     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Editor     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Fortsetzen](updating-components-for-an-upgrade.md)

 

 



