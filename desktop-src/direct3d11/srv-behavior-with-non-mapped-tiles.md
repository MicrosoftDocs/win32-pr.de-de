---
title: SRV-verhalten bei nicht zugeordneten Kacheln
description: Das Verhalten von Lesevorgängen in der Shader-Ressourcen Ansicht (SRV), die nicht zugeordnete Kacheln einschließen, hängt von der Hardwareunterstützung ab.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206228"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>SRV-verhalten bei nicht zugeordneten Kacheln

Das Verhalten von Lesevorgängen in der Shader-Ressourcen Ansicht (SRV), die nicht zugeordnete Kacheln einschließen, hängt von der Hardwareunterstützung ab. Eine Aufschlüsselung der Anforderungen finden Sie unter Read-Behavior für [Kachel Ressourcen-Funktionsebenen](tiled-resources-features-tiers.md). In diesem Abschnitt wird das ideale Verhalten zusammengefasst, das für [Ebene 2](tier-2.md) erforderlich ist.

Stellen Sie sich einen Textur Filter Vorgang vor, der aus einer Gruppe von texeln in einem SRV liest. Texels, die auf nicht zugeordnete Kacheln fallen, tragen in alle nicht fehlenden Komponenten des Formats (und die Standardeinstellung für fehlende Komponenten) in den gesamten Filter Vorgang neben den Beiträgen aus zugeordneten texeln den Wert 0 (null) ein. Die texeln werden alle gewichtet und kombiniert, unabhängig davon, ob die Daten von zugeordneten oder nicht zugeordneten Kacheln stammen.

Die Hardware der ersten Ebene der Ebene [2](tier-2.md) erfüllt diese Spezifikations Anforderung nicht und gibt das 0 (null) mit den Standardwerten zurück, die vorher als Gesamt Filterergebnis bezeichnet werden, wenn texeln (mit einer Gewichtung ungleich null) auf nicht zugeordnete Kacheln fallen. Es ist nicht zulässig, dass andere Hardware die Anforderung erhält, alle texeln (ungleich 0) in den Filter einzubeziehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




