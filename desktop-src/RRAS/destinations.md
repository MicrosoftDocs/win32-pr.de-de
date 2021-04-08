---
title: Destinations
description: Ein Ziel in der Routing Tabelle ist ein Netzwerk Eintrag, der durch eine Netzwerkadresse und eine Netzwerk Maske repräsentiert wird.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856279"
---
# <a name="destinations"></a>Destinations

Ein Ziel in der Routing Tabelle ist ein Netzwerk Eintrag, der durch eine Netzwerkadresse und eine Netzwerk Maske repräsentiert wird.

Ein Ziel Eintrag in der Routing Tabelle umfasst Folgendes:

-   Die Adresse, ausgedrückt als Netzwerkadresse und Netzwerk Maske.
-   Eine Liste der Routen zum Ziel.
-   Eine Liste der nicht transparenten Zeiger Slots.
-   Die Sichten, in denen dieses Ziel gültig ist. Das Ziel enthält eine Struktur für jede Ansicht, die die folgenden Informationen enthält:
    -   Ein Bezeichner für die Sicht.
    -   Ein Zeiger auf die beste Route zum Ziel in dieser Ansicht.
    -   Der Besitzer der optimalen Route in dieser Ansicht.
    -   Flags, die der optimalen Route in dieser Ansicht zugeordnet sind.
    -   Handle für alle Routen, die sich in der Ansicht in einem halte Zustand befinden.

 

 




