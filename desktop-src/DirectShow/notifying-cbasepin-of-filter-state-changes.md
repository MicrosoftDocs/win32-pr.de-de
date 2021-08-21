---
description: Benachrichtigen von CBasePin über Änderungen des Filterstatus
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Benachrichtigen von CBasePin über Änderungen des Filterstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7193402331f150f88217e2d200279e93314c40a9056f52bc31d8100106d4f960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152994"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Benachrichtigen von CBasePin über Änderungen des Filterstatus

Die **CBasePin-Klasse** wird benachrichtigt, wenn sich der Zustand des besitzenden Filters ändert. Für jeden Zustandsübergang ruft der Filter eine entsprechende Methode auf dem Pin auf, wie in der folgenden Tabelle gezeigt.



| Neuer Filterstatus | CBasePin-Methode                                 |
|------------------|-------------------------------------------------|
| Beendet          | [**CBasePin::Inactive**](cbasepin-inactive.md) |
| Angehalten           | [**CBasePin::Active**](cbasepin-active.md)     |
| Wird ausgeführt          | [**CBasePin::Run**](cbasepin-run.md)           |



 

Die abgeleitete Klasse sollte diese Methoden überschreiben, um auf die Zustandsänderung zu reagieren. Je nach Filter kann der Pin einen Arbeitsthread starten, der Stichproben liefert, die Speicherbelegung committ oder decommitiert usw.

 

 



