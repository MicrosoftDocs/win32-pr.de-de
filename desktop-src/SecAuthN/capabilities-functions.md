---
description: Die Netzwerkanbieter-API gibt eine Funktion mit einer einzelnen Funktion an.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funktionen-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042014"
---
# <a name="capabilities-functions"></a>Funktionen-Funktionen

Die Netzwerkanbieter-API gibt eine Funktion mit einer einzelnen Funktion an. Wenn das Betriebssysteminformationen zu den Funktionen eines Netzwerk Anbieters anfordert, ruft der [*multianbieterrouter*](/windows/desktop/SecGloss/m-gly) (MPR) die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion jedes Netzwerk Anbieters auf, dessen Netzwerk aktiv ist.

Die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion gibt eine Bitmaske zurück, die angibt, welche Funktionen der Netzwerkanbieter-API der Netzwerkanbieter unterstützt. Die **NPgetCaps** -Funktion ist die einzige Funktion, die ein Netzwerkanbieter implementieren muss. Das Betriebssystem ruft diese Funktion auf, um zu bestimmen, welche anderen Funktionen der Netzwerkanbieter-API der Anbieter unterstützt.

 

 
