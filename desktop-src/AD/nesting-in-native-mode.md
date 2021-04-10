---
title: Schachtelung im einheitlichen Modus
description: In der folgenden Liste wird beschrieben, was in einer Gruppe enthalten sein kann, die in einer Domäne im einheitlichen Modus vorhanden ist.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Schachtelung im einheitlichen Modus von AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855399"
---
# <a name="nesting-in-native-mode"></a>Schachtelung im einheitlichen Modus

In der folgenden Liste wird beschrieben, was in einer Gruppe enthalten sein kann, die in einer Domäne im einheitlichen Modus vorhanden ist. Diese Liste gilt auch für Verteiler Gruppen in Domänen mit gemischtem Modus. Der Bereich der Gruppe bestimmt diese Kapselungs Regeln.

-   Eine universelle Gruppe kann andere universelle Gruppen, globale Gruppen und Konten aus beliebigen Domänen innerhalb der Gesamtstruktur enthalten, in der sich diese universelle Gruppe befindet.
-   Eine globale Gruppe kann andere globale Gruppen und Konten aus derselben Domäne enthalten, zu der die Gruppe gehört. Eine globale Gruppe darf keine universellen Gruppen oder eine globale Gruppe oder ein anderes Konto aus einer anderen Domäne enthalten.
-   Eine lokale Gruppe der Domäne kann universelle Gruppen, globale Gruppen und Konten aus beliebigen Domänen oder Gesamtstrukturen enthalten. Eine lokale Gruppe der Domäne kann auch andere lokale Domänen Gruppen aus derselben Domäne enthalten, zu der die Gruppe gehört. Eine lokale Domänen Gruppe darf keine anderen lokalen Gruppen der Domäne aus einer anderen Domäne oder Gesamtstruktur enthalten.

 

 




