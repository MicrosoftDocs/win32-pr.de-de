---
description: ICE62 führt umfassende Prüfungen der isolatedcomponent-Tabelle für Daten aus, die zu unerwartetem Verhalten führen können.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368871"
---
# <a name="ice62"></a>ICE62

ICE62 führt umfassende Prüfungen der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) für Daten aus, die zu unerwartetem Verhalten führen können.

Wenn ein von ICE62 gemeldeter Fehler nicht behoben werden kann, kann dies zu einem Ausfall des isolierten Komponenten Systems auf unterschiedlichste Weise führen. Wenn z. b. das shareddllrefcount-Bit nicht für eine freigegebene Komponente festgelegt ist, kann die Registrierung für die Komponente entfernt werden, wenn eine andere Anwendung diese ComponentID verwendet und deinstalliert wird.

## <a name="result"></a>Ergebnis

ICE62 gibt eine Warnung oder einen Fehler aus, wenn Daten in der isolatedcomponent-Tabelle gefunden werden, die möglicherweise zu unerwartetem Verhalten führen.

## <a name="example"></a>Beispiel

ICE62 meldet die folgenden Fehler und Warnungen für die gezeigten Beispiele.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 wird als Anwendungs Komponente zur Isolation von Component1 aufgeführt. Allerdings verfügt Component2 über einen Registrierungsschlüssel Pfad und stellt keinen gültigen ausführbaren Pfad zur Verfügung, der zum Isolieren der Komponente verwendet werden kann.

Um diesen Fehler zu beheben, verwenden Sie eine andere Komponente als Anwendung für die isolierte Komponente Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 wird als isolierte freigegebene Komponente aufgelistet, aber das shareddllrefcount-Bit ist nicht festgelegt. Dies könnte dazu führen, dass die Lebensdauer der Komponente falsch ist. Wenn eine andere Anwendung diese Komponente verwendet (isoliert oder nicht) und deinstalliert wird, wird die Registrierung für die Komponente entfernt, aber die isolierte Kopie dieser Anwendung bleibt erhalten. Dies verursacht Probleme beim Reparieren und deinstallieren.

Um diesen Fehler zu beheben, legen Sie das shareddllrefcount-Bit für die Komponente fest.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 und Component2 werden von unterschiedlichen Funktionen installiert. Component1 wird von Feature1 installiert, und Component2 wird von Feature2 installiert. Feature1 ist kein übergeordnetes Element von Feature2. Daher ist es möglich, dass die Anwendung installiert wird, jedoch nicht die isolierte Komponente, wodurch die Isolation unterbrochen wird.

Um diesen Fehler zu beheben, fügen Sie der FeatureComponents-Tabelle einen Eintrag hinzu, der Component1 mit derselben Funktion wie (oder einem übergeordneten Feature von) der Funktion, die Component2 installiert, verknüpft.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 weist eine Bedingung in der Komponenten Tabelle auf. Wenn sich diese Bedingung während der Lebensdauer einer Installation auf einem Computer von true in false ändert, ist die isolierte Komponente möglicherweise ohne Registrierungsinformationen verwaist.

Um diese Warnung zu beheben, entfernen Sie die Bedingung, oder erstellen Sie die Bedingung so, dass Sie nie von true in false geändert werden kann.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 ist für Component2 und Component3 isoliert, und die beiden Komponenten werden ebenfalls im gleichen Verzeichnis installiert. Die Anwendungen haben eine isolierte Komponente gemeinsam, aber wenn eine Anwendung entfernt wird, wird die freigegebene Komponente ebenfalls entfernt, sodass die anderen Anwendungen die isolierte Komponente verlieren.

Um diese Warnung zu beheben, installieren Sie die Anwendungen in verschiedenen Verzeichnissen, oder überprüfen Sie, ob für einige der Anwendungen tatsächlich eine isolierte Komponente erforderlich ist.

[Isolatedcomponent-Tabelle](isolatedcomponent-table.md)



| Frei \_ gegebene Komponente | Komponenten \_ Anwendung |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Komponenten Tabelle](component-table.md)



| Komponente  | ComponentID | Verzeichnis\_ | Attribute | Bedingung   | KEYPATH   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | MyCondition | Datei1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | Datei3     |



 

[Featurecomponentstable](featurecomponents-table.md)



| Funktion\_ | Komponente\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion  | Über \_ geordnetes Element |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



