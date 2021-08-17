---
description: Die Netzwerkanbieter-API gibt eine einzelne Funktionenfunktion an.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funktionenfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab47d2c8323131b396640d9154e33749c1716db0d369d3a374f69131468613d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141273"
---
# <a name="capabilities-functions"></a>Funktionenfunktionen

Die Netzwerkanbieter-API gibt eine einzelne Funktionenfunktion an. Wenn das Betriebssystem Informationen zu den Funktionen eines Netzwerkanbieters anfing, ruft der Multiple [*Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) die [**NPGetCaps-Funktion**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) jedes Netzwerkanbieters auf, dessen Netzwerk aktiv ist.

Die [**NPGetCaps-Funktion**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) gibt eine Bitmaske zurück, die angibt, welche Funktionen der Netzwerkanbieter-API der Netzwerkanbieter unterstützt. Die **NPGetCaps-Funktion** ist die einzige Funktion, die ein Netzwerkanbieter implementieren muss. Das Betriebssystem ruft diese Funktion auf, um zu bestimmen, welche anderen Funktionen der Netzwerkanbieter-API der Anbieter unterstützt.

 

 
