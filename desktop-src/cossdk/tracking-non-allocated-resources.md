---
description: Nachverfolgen nicht zugeordneter Ressourcen
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Nachverfolgen nicht zugeordneter Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb356a7e7243c7e6f856a0dfe165440ff0b909545703032a8442bbcced77649d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305240"
---
# <a name="tracking-non-allocated-resources"></a>Nachverfolgen nicht zugeordneter Ressourcen

Der Versender-Manager kann eine Ressource nachverfolgen, die nicht inventarisiert ist, basierend auf der Kenntnis der Lebensdauer des Objekts. Wenn eine nachverfolgte, nicht zugeordnete Ressource frei wird, wird sie zerstört und daher nicht an den Bestand zurückgegeben. Dieser nur nachverfolgte Modus für Ressourcen, deren Erstellung und Zerstörung kostengünstig ist, ist nützlicher als das Speichern im Bestand. Dieser Modus ist auch nützlich für die Verwaltung eines Speichersenders oder für eine Ressource, deren Inventur schwierig ist, da es zu viele verschiedene Typen gibt.

Im Modus "Nur Nachverfolgen" erstellt ein Ressourcenverteilener direkt eine angeforderte Ressource, anstatt den Verwerter zu bitten, eine Ressource aus dem Bestand zu reservieren. Bevor diese Ressource an die anfordernde Anwendungskomponente zurückgesetzt wird, weist der Ressourcensender den Verteiler-Manager an, die Ressource nachverfolgung zu verfolgen. Dadurch wird sichergestellt, dass der Verteiler-Manager dies auch dann tun wird, wenn die Lebensdauer der Komponente beendet ist, auch wenn die Komponente die Ressourcen nicht frei gibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DES COM+-Ressourcensenders](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



