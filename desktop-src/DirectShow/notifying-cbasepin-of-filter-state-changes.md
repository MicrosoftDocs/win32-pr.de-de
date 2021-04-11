---
description: Benachrichtigen von cbasepin mit Filter Zustandsänderungen
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Benachrichtigen von cbasepin mit Filter Zustandsänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341749"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Benachrichtigen von cbasepin mit Filter Zustandsänderungen

Die **cbasepin** -Klasse wird immer dann benachrichtigt, wenn sich der Status des besitzenden Filters ändert. Für jeden Zustandsübergang ruft der Filter eine entsprechende Methode für die PIN auf, wie in der folgenden Tabelle dargestellt.



| Neuer Filter Status | Cbasepin-Methode                                 |
|------------------|-------------------------------------------------|
| Beendet          | [**Cbasepin:: inaktiv**](cbasepin-inactive.md) |
| Angehalten           | [**Cbasepin:: Active**](cbasepin-active.md)     |
| Wird ausgeführt          | [**Cbasepin:: Run**](cbasepin-run.md)           |



 

Die abgeleitete Klasse sollte diese Methoden überschreiben, um auf die Zustandsänderung zu reagieren. Abhängig vom Filter startet die PIN möglicherweise einen Arbeits Thread, der Beispiele bereitstellt, einen Commit oder Decommit für die Arbeitsspeicher Zuweisung durch hat und so weiter.

 

 



