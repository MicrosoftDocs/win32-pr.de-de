---
description: Standardmäßig sollten Benutzer des fiktiven MNP2000-Produkts niemals aktualisierte Dateien wie Baseba01.txt verwenden.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Aktualisieren von Komponenten für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e725653acc7aadbeb3710d3cd6b1ee6dc2971e51d3583f2be279ddfed008d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039240"
---
# <a name="updating-components-for-an-upgrade"></a>Aktualisieren von Komponenten für ein Upgrade

Standardmäßig sollten Benutzer des fiktiven MNP2000-Produkts niemals aktualisierte Dateien wie Baseba01.txt verwenden. Daher sind die aktualisierten Dateien definitionsgemäß nicht mit dem ursprünglichen Produkt kompatibel, und Windows Installer-Komponenten wie Baseball, die diese Dateien enthalten, müssen neue Komponentencodes zugewiesen werden. Neue Dateien, z. B. Opera01.txt, werden als Teil einer neuen Komponente mit einem eindeutigen Komponentencode eingeführt. Da das ursprüngliche Produkt und das Upgrade dieselbe Editor Komponente verwenden, bleibt der Komponentencode dieser Komponente unverändert. Weitere Informationen dazu, wann Komponentencode geändert werden muss, finden Sie unter [Ändern des Komponentencodes.](changing-the-component-code.md)

Verwenden Sie Orca oder einen anderen Datenbank-Editor, um die folgenden Daten in die [Component-Tabelle](component-table.md) von MNP2001.msi einzugeben. Verwenden Sie die unten in der ComponentId-Spalte ihres Beispiels gezeigten GUIDs nicht wieder.

[Komponententabelle](component-table.md)



| Komponente  | Componentid                            | Verzeichnis\_ | Attribute | Bedingung | Keypath      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| Basketball | {E1AAB6B0-FEC6-4F18-B765-3B05A81CB} | SPORTDIR    | 2          |           | Basket01.txt |
| Konzert    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | SIDEDIR     | 2          |           | Concer01.txt |
| Tanz      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | SIDEDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | SIDEDIR     | 2          |           | Opera01.txt  |
| Fußball   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Hilfe       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | MONDIR      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| Memorial   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| Editor    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[Fortsetzen](updating-features-for-an-upgrade.md)

 

 



