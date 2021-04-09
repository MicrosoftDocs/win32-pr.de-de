---
description: Entwurfs bedingt sollten Benutzer des fiktiven MNP2000-Produkts niemals aktualisierte Dateien wie Baseba01.txt verwenden.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Aktualisieren von Komponenten für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 920bc955d3d3615941ef03ec885ca8871f79dc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960477"
---
# <a name="updating-components-for-an-upgrade"></a>Aktualisieren von Komponenten für ein Upgrade

Entwurfs bedingt sollten Benutzer des fiktiven MNP2000-Produkts niemals aktualisierte Dateien wie Baseba01.txt verwenden. Daher sind die aktualisierten Dateien definitionsgemäß mit dem ursprünglichen Produkt und den Windows Installer Komponenten (z. b. Baseball) nicht kompatibel, die diese Dateien enthalten, müssen neue Komponenten Codes zugewiesen werden. Neue Dateien, z. b. Opera01.txt, werden als Teil einer neuen Komponente mit einem eindeutigen Komponenten Code eingeführt. Da für das ursprüngliche Produkt und das Upgrade dieselbe Notepad-Komponente verwendet wird, bleibt der Komponenten Code dieser Komponente unverändert. Weitere Informationen zu den Komponenten Codes, die geändert werden müssen, finden Sie unter [Ändern des Komponenten Codes](changing-the-component-code.md).

Verwenden Sie für die Verwendung von Orca oder eines anderen Daten Bank Editors die folgenden Daten in die [Komponenten Tabelle](component-table.md) MNP2001.msi. Verwenden Sie die unten gezeigten GUIDs in der Spalte ComponentID in Ihrem Beispiel nicht.

[Komponenten Tabelle](component-table.md)



| Komponente  | ComponentID                            | Verzeichnis\_ | Attribute | Bedingung | KEYPATH      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Ball   | {2951190a-6af8-4d7f-AA16-d256405c277a} | Sportdir    | 2          |           | Baseba01.txt |
| Erinnen | {E1AAB6B0-FEC6-4F18-B765-3B05A81CEACB} | Sportdir    | 2          |           | Basket01.txt |
| Konzert    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | Argsdir     | 2          |           | Concer01.txt |
| Abhängigkeit      | {1ac2b14d-d5f 4-4642-9F a-ee81bf 59b3e2} | Argsdir     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | Argsdir     | 2          |           | Opera01.txt  |
| Verbandes   | {92aa30f4-7ac5-4dfa-801E-988cf3daa4dc} | Sportdir    | 2          |           | Footba01.txt |
| Hilfe       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | Notepaddir  | 2          |           | Help.txt     |
| January    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | Mondir      | 2          |           | Janua01.txt  |
| Newyears   | {1eef8c53-f C0-405c-8fe3-2b0fe54b0114} | Holdir      | 2          |           | NewYea01.txt |
| Denkmals   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | Holdir      | 2          |           | Memori01.txt |
| Editor    | {19bed232-30ab-11d3-91d3-00c04f d70856} | Notepaddir  | 2          |           | Redpark.exe  |



 

[Fortsetzen](updating-features-for-an-upgrade.md)

 

 



