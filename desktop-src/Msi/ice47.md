---
description: ICE47 überprüft die Tabellen Feature und FeatureComponents auf Features mit 1600 oder mehr Komponenten.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcf1f71af9bb8784c15b159836d329a94e7e6f33b34c31cbba72f9b31349a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381950"
---
# <a name="ice47"></a>ICE47

ICE47 überprüft die Tabellen [Feature](feature-table.md) und [FeatureComponents auf](featurecomponents-table.md) Features mit 1600 oder mehr Komponenten.

## <a name="result"></a>Ergebnis

ICE47 sendet eine Fehlermeldung, wenn ein Feature den maximalen Grenzwert von 1.600 Komponenten pro Feature überschreitet.

## <a name="example"></a>Beispiel

ICE47 meldet die folgende Warnung:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Featuretabelle](feature-table.md) (teilweise)



| Komponente  |
|----------|
| Feature1 |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Aktion   | Bedingung     |
|----------|---------------|
| Feature1 | Komponente1    |
| Feature1 | Component1600 |



 

Um diese Warnung zu beheben, versuchen Sie, das Feature in mehrere Features aufzuteilen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



