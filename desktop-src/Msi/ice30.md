---
description: ICE30 überprüft, ob die Installation von Komponenten, die die gleiche Datei enthalten, die Datei nie mehr als einmal im selben Verzeichnis installiert.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba807ec1eb3bde54b1f115e93c531f24414b75e7a293c8ff1b7d7ff1d3abca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528660"
---
# <a name="ice30"></a>ICE30

ICE30 überprüft, ob die Installation von Komponenten, die die gleiche Datei enthalten, die Datei nie mehr als einmal im selben Verzeichnis installiert.

ICE30 wechselt zu jeder Komponente in der [Tabelle Komponente](component-table.md) und bestimmt dann das Zielverzeichnis der Komponente aus der [Verzeichnistabelle](directory-table.md). Anschließend wird überprüft, welche dieser Komponenten im selben Zielverzeichnis installiert werden. Schließlich wird die [Dateitabelle](file-table.md) verwendet, um zu überprüfen, ob keine der Dateien in diesen Komponenten den gleichen Namen hat.

ICE30 überprüft sowohl lange Dateinamen (Long File Names, LFN) als auch kurze Dateinamen (Short File Names, SFN).

ICE30 wertet keine Eigenschaften in der Auflösung von Verzeichnissen aus, da sich diese Eigenschaften zur Laufzeit ändern und das Verzeichnisauflösungsschema ändern können. Dies bedeutet, dass ICE30 Dateikonflikte aufgrund von Verzeichnissen mit derselben Eigenschaft in ihren Pfaden erkennen kann, aber keine Konflikte erkennt, die sich aus zwei Eigenschaften mit demselben Wert ergeben.

## <a name="result"></a>Ergebnis

ICE30 sendet eine Fehlermeldung für jedes Komponentenpaar, das die gleiche Datei im gleichen Verzeichnis installiert.

## <a name="example"></a>Beispiel

Im gezeigten Beispiel wird jeder der folgenden Fehler zweimal zurückgegeben.



| ICE30-Fehler oder -Warnung                                                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLER: Die Zieldatei "README.1st" wird in "TARGETDIR \\ PRODUCT" von zwei verschiedenen Komponenten auf einem SFN-System installiert: "Component1" und "Component2". Dadurch wird die Komponentenverweiszählung unterbrochen.                                                                                           | Component1 und Component2 verfügen beide über eine Datei mit dem Namen "READEME.1st". Bei Verwendung kurzer Dateinamen installiert das Installationsprogramm sowohl Dir1 als auch Dir2 im gleichen Verzeichnis( TARGETDIR \\ PRODUCT).<br/> ICE30 generiert zwei Fehler, einen für jede Datei. In einer Erstellungsumgebung, in der Fehlerspeicherorte angezeigt werden, befindet sich der erste Fehler im Eintrag einer Datei in der [Dateitabelle](file-table.md)und der zweite am Speicherort der anderen Datei.<br/> |
| FEHLER: Die Installation einer bedingten Komponente würde dazu führen, dass die Zieldatei "README.1st" in "TARGETDIR \\ COMMON TOOLS" von zwei verschiedenen Komponenten auf einem LFN-System installiert wird: "Component3" und "Component4". Dadurch würde die Komponentenverweiszählung unterbrochen.                      | Component4 enthält einen Eintrag in der Spalte Bedingung der [Tabelle Komponente,](component-table.md) component3 nicht. Wenn [**VersionNT**](versionnt.md) true ist, wird Component4 installiert, und es kommt zu einem Konflikt mit readme.1st, der immer von Component3 installiert wird.<br/> ICE30 generiert vier Fehler, ein Paar für SFN, eins für LFN.<br/>                                                                                            |
| WARNUNG: Die Zieldatei "README.1st" kann in "TARGETDIR \\ COMMON TOOLS" von zwei verschiedenen bedingten Komponenten auf einem SFN-System installiert werden: "Component4" und "Component5". Wenn sich die Bedingungen nicht gegenseitig ausschließen, wird das Komponentenverweiszählungssystem unterbrochen. | Da Component4 und Component5 beide Einträge in der Condition -Spalte der [Component-Tabelle](component-table.md) enthalten, tritt dieser Dateikonflikt möglicherweise nicht auf. ICE30 gibt nur eine Warnung aus, da die Bedingungen zum Zeitpunkt der Installation bestimmt werden müssen.<br/> ICE30 generiert vier Warnungen, ein Paar für SFN, eine für LFN.<br/>                                                                                            |



 

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | Verzeichnis | Bedingung |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Komponente4 | Dir3      | VersionNT |
| Komponente5 | Dir3      | Version9x |



 

[Verzeichnistabelle](directory-table.md)



| Verzeichnis | Übergeordnetes \_ Verzeichnis | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | Targetdir                     |
| Dir1      | SOURCEDIR         | Product \| Component1 Product:. |
| Dir2      | SOURCEDIR         | Produkt:.                     |
| Dir3      | SOURCEDIR         | Allgemeine \| Tools:         |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Komponente\_ | FileName   |
|-------|-------------|------------|
| Datei1 | Component1  | README.1st |
| Datei2 | Component2  | README.1st |
| Datei3 | Component3  | README.1st |
| Datei4 | Komponente4  | README.1st |
| Datei5 | Komponente5  | README.1st |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




