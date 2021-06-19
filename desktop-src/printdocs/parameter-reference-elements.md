---
description: Erfahren Sie mehr über ParameterRef-Elemente im Druckschemaframework. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: ParameterRef-Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396525"
---
# <a name="parameterref-elements"></a>ParameterRef-Elemente

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

ParameterRef-Elemente gelten speziell für Option-Elemente, sodass dieses Option-Element auf ein bestimmtes ParameterDef-Element verweisen kann. Für diese Option-Elemente wird ein ScoredProperty-Element, das die Option kennzeichnet, im PrintCapabilities-Dokument nicht als Wert hart codiert, sondern ist stattdessen variabel. Um diese Variabilität zu ermöglichen, enthalten diese ScoredProperty-Elemente ein ParameterRef-Element. Ein ScoredProperty-Element darf nicht sowohl ein Value-Element als auch ein ParameterRef-Element enthalten. Optionselemente, die ein oder mehrere ParameterRef-Elemente enthalten, werden als parametrisierte Option-Elemente bezeichnet.

Das Druckschemaframework ermöglicht es einem Option-Element, eine beliebige Anzahl von ScoredProperty-Elementen, die auf Parameter-Elemente verweisen, zusammen mit einer beliebigen Anzahl von ScoredProperty-Elementen, die Value-Elemente enthalten, zu enthalten. Das Framework lässt auch zu, dass eine beliebige Anzahl von Feature-Elementen parametrisierte Option-Elemente enthält, und eine beliebige Anzahl parametrisierter Option-Elemente ist für jedes Feature-Element zulässig. Außerdem kann auf das gleiche Parameterkonstrukt von mehreren verschiedenen Option-Elementen, Option-Elementen, die zu denselben oder verschiedenen Feature-Elementen gehören können, verwiesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



