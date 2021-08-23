---
title: Schachteln im nativ-Modus
description: In der folgenden Liste wird beschrieben, was in einer Gruppe enthalten sein kann, die in einer Domäne im nativen Modus vorhanden ist.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Schachtelung in AD im nativ-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3fa2842981354738cd4ef112ef278fa33ca310adeedcd62fb245a2663cce07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025738"
---
# <a name="nesting-in-native-mode"></a>Schachteln im nativ-Modus

In der folgenden Liste wird beschrieben, was in einer Gruppe enthalten sein kann, die in einer Domäne im nativen Modus vorhanden ist. Diese Liste gilt auch für Verteilergruppen in Domänen im gemischten Modus. Der Bereich der Gruppe bestimmt diese Ein containment-Regeln.

-   Eine universelle Gruppe kann andere universelle Gruppen, globale Gruppen und Konten aus jeder Domäne innerhalb der Gesamtstruktur enthalten, in der sich diese universelle Gruppe befindet.
-   Eine globale Gruppe kann andere globale Gruppen und Konten aus derselben Domäne enthalten, zu der die Gruppe gehört. Eine globale Gruppe darf keine universellen Gruppen oder globale Gruppen oder Konten aus einer anderen Domäne enthalten.
-   Eine lokale Domänengruppe kann universelle Gruppen, globale Gruppen und Konten aus jeder Domäne oder Gesamtstruktur enthalten. Eine lokale Domänengruppe kann auch andere lokale Domänengruppen aus derselben Domäne enthalten, zu der die Gruppe gehört. Eine lokale Domänengruppe kann keine anderen lokalen Domänengruppen aus einer anderen Domäne oder Gesamtstruktur enthalten.

 

 




