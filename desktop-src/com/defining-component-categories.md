---
title: Definieren von Komponenten Kategorien
description: Definieren von Komponenten Kategorien
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207438"
---
# <a name="defining-component-categories"></a>Definieren von Komponenten Kategorien

Der Autor einer Komponenten Kategoriedefinition erstellt eine eindeutige GUID (die CATID), die zusammen mit der Definition veröffentlicht wird. Andere Parteien kennen die Definition dieses Typs und können die unterstützten Klassen entsprechend verwenden. Wie die Methoden Signatur einer Schnittstelle sollte die Semantik einer Kategorie nach der Installation nicht geändert werden. Es ist besser, die Abwärtskompatibilität der Kategorie zu gewährleisten, indem Sie einen neuen Kategoriebezeichner mit überarbeiteten Semantik einführen.

Da Schnittstellen Bezeichner (IID) und komponentenkategoriebezeichner (CATID) in unterschiedlichen Namespaces vorhanden sind, scheint es so, als ob es möglich wäre, dieselbe GUID für eine IID und eine CATID zu verwenden. Da IIDs jedoch häufig für die CLSID des Proxy-/stubservers der Schnittstelle verwendet werden, besteht ein Konfliktpotenzial. Verwenden Sie daher nicht dieselbe GUID für eine IID und eine CATID.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisierung nach Komponenten Funktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Kategorisierung nach Container Funktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und-Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Der Komponenten Kategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




