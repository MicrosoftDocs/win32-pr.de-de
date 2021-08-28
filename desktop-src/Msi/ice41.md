---
description: ICE41 überprüft, ob die Einträge in den Klassen- und Erweiterungstabellen auf Einträge in der Component-Tabelle verweisen, die das Klassenobjekt oder die Erweiterung der Komponente implementieren.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c220e43cf8a275e520f5babe1ca609a1cee2194b4c08f8dcdafabe6d73bdca4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581110"
---
# <a name="ice41"></a>ICE41

ICE41 überprüft, ob die Einträge in den [Klassen-](class-table.md) und [Erweiterungstabellen](extension-table.md) auf Einträge in der [Component-Tabelle](component-table.md) verweisen, die das Klassenobjekt oder die Erweiterung der Komponente implementieren.

## <a name="result"></a>Ergebnis

ICE41 gibt einen Fehler aus, wenn ein Feature vorhanden ist, das nicht die Komponente enthält, die das Klassenobjekt oder die Erweiterung implementiert.

## <a name="example"></a>Beispiel

ICE41 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE41-Fehler                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Klasse {00000000-0000-0000-0000-0000000000000} verweist auf Feature Feature2 und Komponente Component1, aber die Komponente ist diesem Feature in der Tabelle FeatureComponents nicht zugeordnet. | Es gibt ein Feature, das nicht die Komponente enthält, die das Klassenobjekt implementiert. Dies bedeutet, dass das Installationsprogramm die Komponente nicht mit dem Feature installiert und die Ankündigung möglicherweise nicht wie erwartet funktioniert. Um diesen Fehler zu beheben, ändern Sie den Eintrag in der Spalte Feature \_ des [Klassentabelleneintrags](class-table.md) so, dass er auf ein Feature verweist, das die in der Spalte Komponente aufgeführte Komponente \_ installiert, oder ändern Sie das Feature und die Komponente, die in der [Tabelle FeatureComponents](featurecomponents-table.md)zugeordnet sind.<br/>          |
| Die Erweiterung .yip verweist auf Feature1 und Komponente Component2, aber die Komponente ist diesem Feature in der Tabelle FeatureComponents nicht zugeordnet.                                | Es gibt ein Feature, das die Komponente, die die Erweiterung implementiert, nicht enthält. Dies bedeutet, dass das Installationsprogramm die Komponente nicht mit dem Feature installiert und die Ankündigung möglicherweise nicht wie erwartet funktioniert. Um diesen Fehler zu beheben, ändern Sie den Eintrag in der Spalte Feature \_ des [Tabelleneintrags Erweiterung](extension-table.md) so, dass er auf ein Feature verweist, das die in der Spalte Komponente aufgeführte Komponente \_ installiert, oder ändern Sie das Feature und die Komponente, die in der [Tabelle FeatureComponents](featurecomponents-table.md)zugeordnet sind.<br/> |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Feature\_ |
|-----------|
| Feature1  |
| Feature2  |



 

[Klassentabelle](class-table.md) (partiell)



| CLSID                                  | Komponente\_ | Feature\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Component1  | Feature2  |



 

[Klassentabelle](class-table.md) (partiell)



| Erweiterung | Komponente\_ | Feature\_ |
|-----------|-------------|-----------|
| .yip      | Component2  | Feature1  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




