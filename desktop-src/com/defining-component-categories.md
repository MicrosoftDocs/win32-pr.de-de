---
title: Definieren von Komponentenkategorien
description: Definieren von Komponentenkategorien
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840c785f4b263f0288793f62542cc6d93637b719ff37c9cf29454f43dfaa1914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071010"
---
# <a name="defining-component-categories"></a>Definieren von Komponentenkategorien

Der Autor einer Komponentenkategoriedefinition erstellt eine eindeutige GUID (die CATID), die zusammen mit der Definition veröffentlicht wird. Andere Parteien kennen die Definition dieses Typs und können die unterstützten Klassen entsprechend verwenden. Wie die Methodensignatur einer Schnittstelle sollte die Semantik einer Kategorie nach der Installation nicht geändert werden. Es ist besser, die Abwärtskompatibilität der Kategorie beizubehalten, indem Sie einen neuen Kategoriebezeichner mit überarbeiteter Semantik einführen.

Da Schnittstellenbezeichner (IID) und Komponentenkategoriebezeichner (CATID) in unterschiedlichen Namespaces vorhanden sind, scheint es möglich zu sein, dieselbe GUID sowohl für eine IID als auch für eine CATID zu verwenden. Da IIDs jedoch häufig für die CLSID des Proxy-/Stubservers der Schnittstelle verwendet werden, besteht die Möglichkeit eines Konflikts. Verwenden Sie daher nicht dieselbe GUID für eine IID und CATID.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisieren nach Komponentenfunktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Kategorisieren nach Containerfunktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Der Komponentenkategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




