---
title: Temporale Lokalität
description: Temporale Lokalität ist eine Vermeidungsstrategie, die das Fenster für Teil Aktualisierungen reduziert.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470836"
---
# <a name="temporal-locality"></a>Temporale Lokalität

*Temporale Lokalität* ist eine Vermeidungsstrategie, die das Fenster für Teil Aktualisierungen reduziert. Die Replikation von Änderungen von einem bestimmten Quell Replikat wird in aufsteigender Reihenfolge der Anwendungen fortgesetzt Schreibvorgänge, die gleichzeitig ausgeführt werden, verfügen über Verwendungen, die einander "nah" sind und in der Zeit nah verteilt werden. Anwendungen, die mehrere verknüpfte Objekte erstellen oder aktualisieren, sollten die Objekte möglichst nah beieinander schreiben. Die Anwendung kann z. b. alle notwendigen Eingaben vom Benutzer erfassen und auf das Verzeichnis anwenden, wenn der Benutzer auf die Schaltfläche "anwenden" klickt.

Temporale Lokalität verringert außerdem die Wahrscheinlichkeit einer Konfliktlösung, die interne Inkonsistenzen einführt.

 

 




