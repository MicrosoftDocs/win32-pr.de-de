---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: ParameterRef-Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050732"
---
# <a name="parameterref-elements"></a>ParameterRef-Elemente

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

ParameterRef-Elemente gelten speziell für options Elemente, sodass das Option-Element auf ein bestimmtes ParameterDef-Element verweisen kann. Für diese Options Elemente ist ein ScoredProperty-Element, das die Option kennzeichnet, im printfunktionalitäten-Dokument nicht als Wert hart codiert, sondern ist eine Variable. Diese ScoredProperty-Elemente enthalten ein ParameterRef-Element, um diese Variabilität zu aktivieren. Ein ScoredProperty-Element darf nicht sowohl ein Value-Element als auch ein ParameterRef-Element enthalten. Options Elemente, die ein oder mehrere ParameterRef-Elemente enthalten, werden als parametrisierte Options Elemente bezeichnet.

Das Print Schema-Framework ermöglicht, dass ein Option-Element eine beliebige Anzahl von ScoredProperty-Elementen enthält, die auf Parameter Elemente verweisen, sowie eine beliebige Anzahl von ScoredProperty-Elementen, die value-Elemente enthalten. Das Framework ermöglicht außerdem, dass eine beliebige Anzahl von Featureelementen parametrisierte Options Elemente enthalten kann, und jede beliebige Anzahl von parametrisierten Options Elementen ist für jedes Feature-Element zulässig. Außerdem kann auf dasselbe Parameter Konstrukt durch mehrere unterschiedliche Options Elemente verwiesen werden, Options Elemente, die zu denselben oder unterschiedlichen Funktions Elementen gehören können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



