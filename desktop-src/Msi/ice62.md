---
description: ICE62 führt umfangreiche Überprüfungen der Tabelle IsolatedComponent auf Daten durch, die zu unerwartetem Verhalten führen können.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5c2fd3f3305c791851fb3bd7480edc5e17f361c40719e8091930188dfa991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528240"
---
# <a name="ice62"></a>ICE62

ICE62 führt umfangreiche [Überprüfungen der Tabelle IsolatedComponent](isolatedcomponent-table.md) auf Daten durch, die zu unerwartetem Verhalten führen können.

Wenn ein von ICE62 gemeldeter Fehler nicht behoben wird, kann dies auf viele verschiedene Arten zu einem Ausfall des isolierten Komponentensystems führen. Wenn beispielsweise das SharedDllRefCount-Bit nicht für eine freigegebene Komponente festgelegt ist, kann die Registrierung für die Komponente entfernt werden, wenn eine andere Anwendung diese ComponentId verwendet und deinstalliert wird.

## <a name="result"></a>Ergebnis

ICE62 sendet eine Warnung oder einen Fehler, wenn Daten in der Tabelle IsolatedComponent gefunden werden, die zu unerwartetem Verhalten führen können.

## <a name="example"></a>Beispiel

ICE62 meldet die folgenden Fehler und Warnungen für die gezeigten Beispiele.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 wird als Anwendungskomponente für die Isolation von component1 aufgeführt. Component2 verfügt jedoch über einen Registrierungsschlüsselpfad und stellt keinen gültigen ausführbaren Pfad bereit, der zum Isolieren der Komponente verwendet werden kann.

Um diesen Fehler zu beheben, verwenden Sie eine andere Komponente als Anwendung für die isolierte Komponente Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 ist als isolierte freigegebene Komponente aufgeführt, aber das SharedDllRefCount-Bit ist nicht festgelegt. Dies kann dazu führen, dass die Lebensdauer der Komponente falsch ist. Wenn eine andere Anwendung diese Komponente verwendet (isoliert oder nicht) und deinstalliert wird, wird die Registrierung für die Komponente entfernt, aber die isolierte Kopie dieser Anwendung bleibt erhalten. Dies führt zu Reparatur- und Deinstallationsproblemen.

Um diesen Fehler zu beheben, legen Sie das SharedDllRefCount-Bit für die Komponente fest.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 und Component2 werden von verschiedenen Features installiert. Component1 wird von Feature1 und Component2 von Feature2 installiert. Feature1 ist kein übergeordnetes Feature von Feature2. Daher ist es möglich, dass die Anwendung installiert wird, aber nicht die isolierte Komponente, wodurch die Isolation aufgehoben wird.

Um diesen Fehler zu beheben, fügen Sie der Tabelle FeatureComponents einen Eintrag hinzu, der Component1 mit demselben Feature verknüpft wie (oder ein übergeordnetes Feature des Features), das Component2 installiert.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 weist eine Bedingung in der Tabelle Component auf. Wenn sich diese Bedingung während der Lebensdauer einer Installation auf einem Computer von TRUE in FALSE ändert, kann die isolierte Komponente ohne Registrierungsinformationen verwaist sein.

Um diese Warnung zu beheben, entfernen Sie die Bedingung, oder erstellen Sie die Bedingung, damit sie nie von TRUE in FALSE geändert werden kann.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 ist sowohl für Component2 als auch für Component3 isoliert, und die beiden Komponenten werden ebenfalls im gleichen Verzeichnis installiert. Die Anwendungen teilen sich eine isolierte Komponente, aber wenn eine Anwendung entfernt wird, wird auch die freigegebene Komponente entfernt, sodass die anderen Anwendungen die isolierte Komponente verlieren.

Um diese Warnung zu beheben, installieren Sie die Anwendungen in verschiedenen Verzeichnissen, oder überprüfen Sie, ob einige der Anwendungen tatsächlich eine isolierte Komponente benötigen.

[IsolatedComponent-Tabelle](isolatedcomponent-table.md)



| \_Komponente freigegeben | \_Komponentenanwendung |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Komponententabelle](component-table.md)



| Komponente  | Componentid | Verzeichnis\_ | Attribute | Bedingung   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | MYCONDITION | Datei1     |
| Component2 |             | Targetdir   | 4          |             | Registry2 |
| Component3 |             | Targetdir   | 0          |             | Datei3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Feature\_ | Komponente\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[Featuretabelle](feature-table.md) (teilweise)



| Feature  | \_Übergeordnetes Feature |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



