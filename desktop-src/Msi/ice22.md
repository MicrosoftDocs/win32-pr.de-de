---
description: ICE22 verwendet die Tabelle FeatureComponents, um die Zuordnung von Features und Komponenten zu überprüfen, auf die in der PublishComponent-Tabelle verwiesen wird.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177fcef5441e5b82738c76face70427cc6865ae59c11542fca080b3dc521c5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529020"
---
# <a name="ice22"></a>ICE22

ICE22 verwendet die [Tabelle FeatureComponents,](featurecomponents-table.md) um die Zuordnung von Features und Komponenten zu überprüfen, auf die in der [PublishComponent-Tabelle](publishcomponent-table.md)verwiesen wird.

## <a name="result"></a>Ergebnis

ICE22 sendet eine Fehlermeldung, wenn die Features und Komponenten in der [PublishComponent-Tabelle](publishcomponent-table.md)falsch zugeordnet sind.

## <a name="example"></a>Beispiel

Im folgenden Beispiel sendet ICE22 einen Fehler, {00000003-0004-0000-0000-624474732465} der nicht über die richtige Zuordnung für die Spalten Feature und Component \_ \_ verfügt.

[PublishComponent-Tabelle](publishcomponent-table.md) (partiell)



| Componentid                            | Feature\_ | Komponente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Feature\_ | Komponente\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



