---
description: ICE22 verwendet die FeatureComponents-Tabelle, um die Zuordnung von Features und Komponenten zu überprüfen, auf die in der PublishComponent-Tabelle verwiesen wird.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347662"
---
# <a name="ice22"></a>ICE22

ICE22 verwendet die [FeatureComponents-Tabelle](featurecomponents-table.md) , um die Zuordnung von Features und Komponenten zu überprüfen, auf die in der [PublishComponent-Tabelle](publishcomponent-table.md)verwiesen wird.

## <a name="result"></a>Ergebnis

ICE22 gibt eine Fehlermeldung aus, wenn die Features und Komponenten in der [Tabelle PublishComponent](publishcomponent-table.md)nicht ordnungsgemäß zugeordnet sind.

## <a name="example"></a>Beispiel

Im folgenden Beispiel gibt ICE22 einen Fehler aus, {00000003-0004-0000-0000-624474732465} der nicht über die richtige Zuordnung für die Funktion \_ und die Komponenten \_ Spalten verfügt.

[PublishComponent-Tabelle](publishcomponent-table.md) (partiell)



| ComponentID                            | Funktion\_ | Komponente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Funktion\_ | Komponente\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



