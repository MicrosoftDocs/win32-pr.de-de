---
title: Verwenden undurchsichtiger Zeiger
description: Clients müssen häufig zusätzliche Client spezifische Informationen zu Zielen speichern.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856532"
---
# <a name="using-opaque-pointers"></a>Verwenden undurchsichtiger Zeiger

Clients müssen häufig zusätzliche Client spezifische Informationen zu Zielen speichern. Mithilfe des Routing Tabellen-Managers können Clients diese Informationen in Zielstrukturen in der Routing Tabelle speichern. Die Informationen werden mithilfe von nicht transparenten *Zeigern* gespeichert und abgerufen. Die gespeicherten Informationen sind privat und können nur für den Client zugänglich sein, der den nicht transparenten Zeiger besitzt.

Beispielsweise behält der Multicast-Gruppen-Manager eine Liste von Multicast-Weiterleitungs Einträgen bei, die von einem bestimmten Ziel abhängig sind. Der Multicast-Gruppen-Manager verwendet einen nicht transparenten Zeiger in diesem Ziel. In einem anderen Beispiel kann ein Routing Protokoll, das ein bestimmtes Ziel angekündigt hat, Informationen im Zusammenhang mit der eigenen Routen Ankündigung des Ziels mithilfe eines nicht transparenten Zeigers aufbewahren, auch wenn er nicht die beste Route besitzt.

Die Anzahl der nicht transparenten Zeiger ist beschränkt. Diese Zeiger werden den Clients auf der Basis von First-come-first-served-Basis zugewiesen. Der Routeradministrator muss die richtige Anzahl von Zeigern während der Routerkonfiguration zuordnen. Daher müssen Routing Protokolle und andere Clients ihre Verwendung undurchsichtiger Zeiger dokumentieren.

 

 




