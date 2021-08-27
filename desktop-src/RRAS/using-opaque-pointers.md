---
title: Verwenden von nicht transparenten Zeigern
description: Clients müssen häufig zusätzliche, clientspezifische Informationen zu Zielen speichern.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d24524f64fca7062ffb35ed6f4d5e6a2bc935ef7fee0c7fa141cb2e823e70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025070"
---
# <a name="using-opaque-pointers"></a>Verwenden von nicht transparenten Zeigern

Clients müssen häufig zusätzliche, clientspezifische Informationen zu Zielen speichern. Mit dem Routingtabellen-Manager können Clients diese Informationen in Zielstrukturen in der Routingtabelle speichern. Die Informationen werden *mithilfe von nicht transparenten Zeigern* gespeichert und abgerufen. Die gespeicherten Informationen sind privat und nur für den Client zugänglich, der den nicht transparenten Zeiger besitzt.

Beispielsweise führt der Multicastgruppen-Manager eine Liste von Multicastweiterleitungseinträgen, die von einem bestimmten Ziel abhängig sind. Der Multicastgruppen-Manager verwendet einen nicht transparenten Zeiger in diesem Ziel. In einem anderen Beispiel kann ein Routingprotokoll, das ein bestimmtes Ziel ankündigt, Informationen im Zusammenhang mit seiner eigenen Routenankündigung des Ziels mithilfe eines nicht transparenten Zeigers beibehalten, obwohl es nicht die beste Route besitzt.

Die Anzahl der nicht transparenten Zeiger ist begrenzt. diese Zeiger werden Clients auf der Basis von "First Come" und "First-Served" zugeordnet. Der Routeradministrator muss während der Routerkonfiguration die richtige Anzahl von Zeigern zuordnen. Daher müssen Routingprotokolle und andere Clients ihre Verwendung von nicht transparenten Zeigern dokumentieren.

 

 




