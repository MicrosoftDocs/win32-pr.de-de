---
description: ICE30 überprüft, ob die Installation von Komponenten, die dieselbe Datei enthalten, die Datei nie mehrmals im gleichen Verzeichnis installiert.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360648"
---
# <a name="ice30"></a>ICE30

ICE30 überprüft, ob die Installation von Komponenten, die dieselbe Datei enthalten, die Datei nie mehrmals im gleichen Verzeichnis installiert.

ICE30 wechselt zu jeder Komponente in der [Komponenten Tabelle](component-table.md) und bestimmt dann das Zielverzeichnis der Komponente aus der [Verzeichnis Tabelle](directory-table.md). Anschließend wird überprüft, welche dieser Komponenten in demselben Zielverzeichnis installiert werden. Schließlich wird anhand der [Dateitabelle](file-table.md) überprüft, ob keine der Dateien in diesen Komponenten denselben Namen hat.

ICE30 prüft sowohl lange Dateinamen (LFN) als auch kurze Dateinamen (SFN).

ICE30 wertet keine Eigenschaften in der Auflösung von Verzeichnissen aus, da sich diese Eigenschaften zur Laufzeit ändern und das Verzeichnis Auflösungs Schema ändern können. Dies bedeutet, dass ICE30 Datei Kollisionen aufgrund von Verzeichnissen mit derselben Eigenschaft in ihren Pfaden erkennen kann, jedoch keine Konflikte erkennt, die sich aus zwei Eigenschaften mit demselben Wert ergeben.

## <a name="result"></a>Ergebnis

ICE30 gibt eine Fehlermeldung für jedes Paar von Komponenten aus, die dieselbe Datei im selben Verzeichnis installiert.

## <a name="example"></a>Beispiel

Im gezeigten Beispiel werden die folgenden Fehler zweimal zurückgegeben.



| ICE30-Fehler oder-Warnung                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler: die Zieldatei "Infodatei. 1st" wird \\ von zwei verschiedenen Komponenten auf einem SFN-System in "TARGETDIR Product" installiert: "Component1" und "Component2". Dadurch wird die Komponenten Verweis Zählung unterbrochen.                                                                                           | Component1 und Component2 verfügen beide über eine Datei mit dem Namen "reademe. 1st". Wenn Sie kurze Dateinamen verwenden, installiert das Installationsprogramm sowohl dir1 als auch dir2 im gleichen Verzeichnis, TARGETDIR \\ Product.<br/> ICE30 generiert zwei Fehler, eine für jede Datei. In einer Erstellungs Umgebung, in der Fehlerspeicher Orte angezeigt werden, liegt der erste Fehler bei einem Datei Eintrag in der [Dateitabelle](file-table.md)und der zweite am Speicherort der anderen Datei.<br/> |
| Fehler: die Installation einer conditionalized-Komponente würde bewirken, dass die Zieldatei "infome. 1st" in "TARGETDIR \\ Common Tools" von zwei verschiedenen Komponenten auf einem LFN-System installiert wird: "Component3" und "Component4". Dadurch wird die Anzahl der Komponenten Verweise nicht mehr berücksichtigt.                      | Component4 verfügt über einen Eintrag in der Condition-Spalte der [Component-Tabelle](component-table.md) und Component3 nicht. Wenn [**VersionNT**](versionnt.md) den Wert true aufweist, wird Component4 installiert, und es gibt einen Konflikt mit der Info. 1. wird immer von Component3 installiert.<br/> ICE30 generiert 4 Fehler, ein paar für SFN, eines für LFN.<br/>                                                                                            |
| Warnung: die Zieldatei "Infodatei. 1st" kann in "TARGETDIR \\ Common Tools" durch zwei unterschiedliche conditionalisierte Komponenten auf einem SFN-System installiert werden: "Component4" und "Component5". Wenn die Bedingungen sich nicht gegenseitig ausschließen, wird das Komponenten Verweis-System unterbrechen. | Da "Component4" und "Component5" in der Spalte "Bedingung" der [Komponenten Tabelle](component-table.md) Einträge enthalten, tritt möglicherweise keine Datei Kollision auf. ICE30 gibt nur dann eine Warnung aus, wenn die Bedingungen zum Zeitpunkt der Installation bestimmt werden müssen.<br/> ICE30 generiert 4 Warnungen, ein paar für SFN, eines für LFN.<br/>                                                                                            |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Verzeichnis | Bedingung |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis | Übergeordnetes \_ Verzeichnis | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Product \| Component1 Product:. |
| Dir2      | SOURCEDIR         | Produkt:.                     |
| Dir3      | SOURCEDIR         | Gängige gängige \| Tools:         |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ | FileName   |
|-------|-------------|------------|
| Datei1 | Component1  | Info. 1. |
| Datei2 | Component2  | Info. 1. |
| Datei3 | Component3  | Info. 1. |
| Datei4 | Component4  | Info. 1. |
| Datei5 | Component5  | Info. 1. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




