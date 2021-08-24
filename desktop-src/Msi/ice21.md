---
description: ICE21 überprüft, ob jede Komponente in der Component-Tabelle zu einem Feature gehört. Sie verwendet die Tabelle FeatureComponents, um diese Zuordnung zu überprüfen.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c5c517bd41c7d777f327606b3672f90b57a821dbbef028fa985acd043e6768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529030"
---
# <a name="ice21"></a>ICE21

ICE21 überprüft, ob jede Komponente in der [Component-Tabelle](component-table.md) zu einem Feature gehört. Sie verwendet die [Tabelle FeatureComponents,](featurecomponents-table.md) um diese Zuordnung zu überprüfen.

## <a name="result"></a>Ergebnis

ICE21 gibt eine Fehlermeldung aus, wenn das Installationspaket eine Komponente enthält, die nicht zu einem Feature gehört.

## <a name="example"></a>Beispiel

Im folgenden Beispiel gibt ICE21 eine Fehlermeldung mit dem Hinweis aus, dass die Komponente Comp1 keinen Features zuteil wird.

[Komponententabelle](component-table.md) (partiell)



| Komponente |
|-----------|
| Comp1     |
| Comp2     |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Feature  | Komponente |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



