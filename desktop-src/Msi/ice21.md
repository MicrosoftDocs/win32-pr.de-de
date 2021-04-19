---
description: ICE21 überprüft, ob jede Komponente in der Komponenten Tabelle zu einer Funktion gehört. Er verwendet die FeatureComponents-Tabelle, um diese Zuordnung zu überprüfen.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348107"
---
# <a name="ice21"></a>ICE21

ICE21 überprüft, ob jede Komponente in der [Komponenten Tabelle](component-table.md) zu einer Funktion gehört. Er verwendet die [FeatureComponents-Tabelle](featurecomponents-table.md) , um diese Zuordnung zu überprüfen.

## <a name="result"></a>Ergebnis

ICE21 gibt eine Fehlermeldung aus, wenn das Installationspaket eine Komponente enthält, die nicht zu einer Funktion gehört.

## <a name="example"></a>Beispiel

Im folgenden Beispiel gibt ICE21 eine Fehlermeldung aus, die besagt, dass die Komponente Comp1 keiner Funktion zugeordnet ist.

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente |
|-----------|
| Comp1     |
| Comp2     |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Funktion  | Komponente |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



