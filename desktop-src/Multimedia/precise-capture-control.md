---
title: Präzise Erfassungssteuerung
description: Präzise Erfassungssteuerung
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- AVICap-Rückruffunktionen, präzise Erfassungssteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365482f5f6309f9642aa5c8b497b58a1d9416e398e5c3624191d777e006b23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372660"
---
# <a name="precise-capture-control"></a>Präzise Erfassungssteuerung

Ein Erfassungsfenster kann der Rückruffunktion capture-control eine präzise Kontrolle über die Zeiten bieten, in denen die Streamingerfassung beginnt und endet. Die erste Nachricht, die vom Erfassungstreiber an die Rückrufprozedur gesendet wird, legt den *nState-Parameter* auf CONTROLCALLBACK PREROLL fest, \_ nachdem alle Puffer und alle anderen Aufzeichnungsvorbereitungen zugewiesen wurden. Diese Meldung gibt der Anwendung die Möglichkeit, die Videoquellen vorab zurollen. (Die Rückruffunktion gibt *nState* als zweiten Parameter an.) Die Rückruffunktion gibt dann zum genauen Zeitpunkt zurück, zu dem die Aufzeichnung beginnen soll. Der Rückgabewert **TRUE** aus der Rückruffunktion setzt die Erfassung fort. Der Rückgabewert **FALSE** bricht die Erfassung ab. Sobald die Erfassung beginnt, wird die Rückruffunktion häufig aufgerufen, wobei *nState* auf CONTROLCALLBACK CAPTUREING festgelegt \_ ist, damit die Anwendung die Erfassung beenden kann, indem **FALSE** zurückgegeben wird.

 

 




