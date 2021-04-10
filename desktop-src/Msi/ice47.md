---
description: ICE47 überprüft die Funktions-und FeatureComponents-Tabellen auf Features mit 1600 oder mehr Komponenten.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215912"
---
# <a name="ice47"></a>ICE47

ICE47 überprüft die [Funktions](feature-table.md) -und [FeatureComponents](featurecomponents-table.md) -Tabellen auf Features mit 1600 oder mehr Komponenten.

## <a name="result"></a>Ergebnis

ICE47 gibt eine Fehlermeldung aus, wenn eine Funktion den maximalen Grenzwert von 1600 Komponenten pro Feature überschreitet.

## <a name="example"></a>Beispiel

ICE47 würde die folgende Warnung melden:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion  |
|----------|
| Feature1 |



 

[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)



| Aktion   | Bedingung     |
|----------|---------------|
| Feature1 | Component1    |
| Feature1 | Component1600 |



 

Um diese Warnung zu beheben, teilen Sie die Funktion in mehrere Funktionen auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



