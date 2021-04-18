---
description: ICE41 überprüft, ob die Einträge in den Klassen-und Erweiterungs Tabellen auf Einträge in der Komponenten Tabelle verweisen, die das Klassenobjekt oder die Erweiterung der Komponente implementieren.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359001"
---
# <a name="ice41"></a>ICE41

ICE41 überprüft, ob die Einträge in den [Klassen](class-table.md) -und [Erweiterungs](extension-table.md) Tabellen auf Einträge in der [Komponenten Tabelle](component-table.md) verweisen, die das Klassenobjekt oder die Erweiterung der Komponente implementieren.

## <a name="result"></a>Ergebnis

ICE41 gibt einen Fehler aus, wenn eine Funktion vorhanden ist, die nicht die Komponente enthält, die das Klassenobjekt oder die Erweiterung implementiert.

## <a name="example"></a>Beispiel

ICE41 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE41-Fehler                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Class {00000000-0000-0000-0000-0000000000000} References Feature Feature2 und Component Component1, aber die Komponente ist nicht mit dieser Funktion in der FeatureComponents-Tabelle verknüpft. | Es gibt eine Funktion, die nicht die Komponente enthält, die das Klassenobjekt implementiert. Dies bedeutet, dass das Installationsprogramm die Komponente nicht mit der Funktion installiert, und dass die Werbung möglicherweise nicht wie erwartet funktioniert. Um diesen Fehler zu beheben, ändern Sie den Eintrag in der \_ featurespalte des [Klassen Tabellen](class-table.md) Eintrags, um auf eine Funktion zu verweisen, mit der die in der Spalte Komponente aufgeführte Komponente installiert wird, \_ oder ändern Sie die Funktion und die Komponente, die in der [FeatureComponents](featurecomponents-table.md)<br/>          |
| Die Erweiterung. Yip verweist auf die Features Feature1 und Component Component2, aber diese Komponente ist nicht mit dieser Funktion in der FeatureComponents-Tabelle verknüpft.                                | Es gibt eine Funktion, die nicht die Komponente enthält, die die Erweiterung implementiert. Dies bedeutet, dass das Installationsprogramm die Komponente nicht mit der Funktion installiert, und dass die Werbung möglicherweise nicht wie erwartet funktioniert. Um diesen Fehler zu beheben, ändern Sie den Eintrag in der \_ featurespalte des [Erweiterungs Tabellen](extension-table.md) Eintrags, um auf eine Funktion zu verweisen, mit der die in der Spalte Komponente aufgeführte Komponente installiert wird, \_ oder ändern Sie die Funktion und die Komponente, die in der [Tabelle FeatureComponents](featurecomponents-table.md)<br/> |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Funktion\_ |
|-----------|
| Feature1  |
| Feature2  |



 

[Klassen Tabelle](class-table.md) (partiell)



| CLSID                                  | Komponente\_ | Funktion\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Component1  | Feature2  |



 

[Klassen Tabelle](class-table.md) (partiell)



| Durchwahl | Komponente\_ | Funktion\_ |
|-----------|-------------|-----------|
| . Yip      | Component2  | Feature1  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




