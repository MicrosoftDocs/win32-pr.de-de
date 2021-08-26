---
description: Um ein Produkt, eine Komponente oder ein Feature zu veröffentlichen, verwenden Sie eine der Veröffentlichungsaktionen.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Veröffentlichen von Produkten, Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dd62e080cf58188405e20d1fd69507f849dd37ceddd01eaf1f4bbe7c59ea76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041990"
---
# <a name="publishing-products-features-and-components"></a>Veröffentlichen von Produkten, Features und Komponenten

Um [ein Produkt,](components-and-features.md) eine Komponente oder ein Feature zu veröffentlichen, verwenden Sie eine der Veröffentlichungsaktionen. Die [PublishProduct-Aktion](publishproduct-action.md) registriert die Produktinformationen beim System. Veröffentlichen Sie nach dem Ausführen der PublishProduct-Aktion die Komponenten mit der [PublishComponents-Aktion,](publishcomponents-action.md)die wiederum die [PublishComponent-Tabelle](publishcomponent-table.md) verwendet, um die Als angekündigt festgelegten Komponenten zu bestimmen. Rufen Sie zum Veröffentlichen pro Feature die [PublishFeatures-Aktion auf.](publishfeatures-action.md) Diese Aktion verwendet die [Tabelle FeatureComponents](featurecomponents-table.md) als Daten, um aufzulösen, welche Features angekündigt werden.

Es gibt auch zwei entsprechende Aktionen, die die Veröffentlichung eines Features oder einer Komponente aufheben: die Aktion [UnpublishComponents](unpublishcomponents-action.md) und die [UnpublishFeatures-Aktion](unpublishfeatures-action.md).

 

 



