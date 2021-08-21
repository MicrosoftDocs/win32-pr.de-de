---
title: Aktualisieren von Routen an Ort und Stelle mit rtmUpdateAndUnlockRoute
description: Das direkte Aktualisieren ist im Allgemeinen effizienter als das Aktualisieren der Routingtabelle mit einer indirekten Methode wie der, die von der RtmAddRouteToDest-Funktion verwendet wird.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfcfdc7abd355cd70bb1295af6ce8b4fb4749dfed6c55af4d1fd06ca8257170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073700"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Aktualisieren von Routen an Ort und Stelle mit rtmUpdateAndUnlockRoute

Das direkte Aktualisieren ist im Allgemeinen effizienter als das Aktualisieren der Routingtabelle mit einer indirekten Methode wie der, die von der [**RtmAddRouteToDest-Funktion verwendet**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) wird. Diese Methode ist effizienter, da der Client weder ein Handle abrufen noch die [**RTM ROUTE \_ \_ INFO-Struktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) an und vom Routingtabellen-Manager übergeben muss. Diese Methode benötigt auch weniger Zeit. Das direkte Aktualisieren der Routingtabelle kann jedoch riskant sein, da der Routingtabellen-Manager nicht als Vermittler fungieren kann.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter Aktualisieren einer Route an Ort und Stelle [mit rtmUpdateAndUnlockRoute.](update-a-route-in-place-using-rtmupdateandunlockroute.md)

 

 




