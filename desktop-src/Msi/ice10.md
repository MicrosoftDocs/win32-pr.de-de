---
description: ICE10 überprüft, ob der Ankündigungsstatus untergeordneter Features mit dem des übergeordneten Features entspricht.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581210"
---
# <a name="ice10"></a>ICE10

ICE10 überprüft, ob der Ankündigungsstatus untergeordneter Features mit dem des übergeordneten Features entspricht.

Eine untergeordnete Funktion lässt möglicherweise keine Ankündigung zu, während das übergeordnete Feature Ankündigungen zulässt. Die folgende Kombination aus übergeordneten und untergeordneten Attributen ist daher ungültig.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Diese Kombination ist ungültig, da sie das übergeordnete Element immer dann deaktivieren würde, wenn das übergeordnete Element angekündigt werden sollte. Das Gegenteil ist jedoch zulässig. Ein untergeordnetes Element kann markiert werden, um die Ankündigung zu bevorzugen, während das übergeordnete Element so markiert ist, dass keine Ankündigung mehr möglich ist.

Die benutzerdefinierte ICE10-Aktion bestimmt den Status von übergeordneten und untergeordneten Features aus der Spalte Attribute der [Featuretabelle.](feature-table.md) Beachten Sie, dass es gültig ist, den Zustand eines Features auf 0 und dessen übergeordnetes oder untergeordnetes Element so zu setzen, dass Ankündigungen bevorzugt oder nicht zulässig sind.

## <a name="result"></a>Ergebnis

ICE10 gibt einen Fehler aus, wenn die Spalte Attribute der [Featuretabelle](feature-table.md) einen Konflikt im Anknungszustand enthält.

## <a name="example"></a>Beispiel

ICE10 veröffentlicht die folgende Fehlermeldung für das gezeigte Beispiel.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

Beachten Sie für dieses Beispiel, dass Microsoft Excel und Microsoft Word untergeordnete Features von Microsoft Office.

[Featuretabelle](feature-table.md) (partiell)



| Feature | Übergeordnetes \_ Feature | Attribute |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

In diesem Beispiel wird Word so festgelegt, dass Keine Ankündigung zulässig ist, die mit dem Zustand der zulässigen Ankündigung des übergeordneten Elements in Konflikt steht, Office.

In einigen Fällen gibt ICE10 den folgenden Fehler aus:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Dies bezieht sich auf einen ungültigen Fremdschlüsselverweis. Das Problem wird behoben, indem "Child" auf das richtige übergeordnete Feature zeigt oder der Featuretabelle einen Eintrag für das übergeordnete Feature ["Parent"](feature-table.md) hinzufüge.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



