---
description: ICE10 überprüft, ob der Ankündigungs Status von untergeordneten Funktionen mit dem des übergeordneten Features übereinstimmt.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357869"
---
# <a name="ice10"></a>ICE10

ICE10 überprüft, ob der Ankündigungs Status von untergeordneten Funktionen mit dem des übergeordneten Features übereinstimmt.

Eine untergeordnete Funktion lässt eine Ankündigung möglicherweise nicht zu, während ihre übergeordnete Funktion eine Ankündigung zulässt. Die folgende Kombination aus über-und untergeordneten Attributen ist daher ungültig.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Diese Kombination ist ungültig, da Sie das übergeordnete Element ausschalten würde, wenn das übergeordnete Element angekündigt werden soll. Der umgekehrte Wert ist jedoch zulässig. Ein untergeordnetes Element kann gekennzeichnet werden, um Ankündigungen zu bevorzugen, während das übergeordnete Element als nicht zulassen gekennzeichnet ist.

Die benutzerdefinierte Aktion ICE10 bestimmt den Status von übergeordneten und untergeordneten Funktionen [in der Spalte](feature-table.md) Attribute der Featuretabelle. Beachten Sie, dass es zulässig ist, den Status einer Funktion auf 0 festzulegen und das übergeordnete oder untergeordnete Element festzulegen, um Ankündigungen zu bevorzugen oder zu unterbinden.

## <a name="result"></a>Ergebnis

ICE10 gibt einen Fehler aus, wenn die Spalte Attribute der [Merkmals](feature-table.md) Tabelle eine fehlende Übereinstimmung im Ankündigungs Status enthält.

## <a name="example"></a>Beispiel

ICE10 gibt die folgende Fehlermeldung für das gezeigte Beispiel aus.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

Beachten Sie in diesem Beispiel, dass Microsoft Excel und Microsoft Word untergeordnete Funktionen von Microsoft Office sind.

[Funktions](feature-table.md) Tabelle (partiell)



| Funktion | Über \_ geordnetes Element | Attribute |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

Im Beispiel wird Word so festgelegt, dass keine Ankündigung zugelassen wird. Dies steht in Konflikt mit dem Status "Ankündigung zulassen" des übergeordneten Office.

In einigen Fällen gibt ICE10 den folgenden Fehler aus:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Dies bezieht sich auf einen ungültigen Fremdschlüssel Verweis. Die Korrektur besteht darin, dass ' Child ' [auf die richtige](feature-table.md) übergeordnete Funktion verweist, oder Sie fügt der Featuretabelle einen Eintrag für das übergeordnete Feature ' Parent ' hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



