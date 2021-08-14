---
description: Stationssätze, die über eine Drittanbieterverbindung überwacht werden, werden als Liniengerät und möglicherweise als zugeordnetes Telefongerät modelliert.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Stationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad9874542a63f05e124ea5df833aa0a433c03713cc3a2d7bb1ca3a471174e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760717"
---
# <a name="stations"></a>Stationen

Stationssätze, die über eine Drittanbieterverbindung überwacht werden, werden als Liniengerät und möglicherweise als zugeordnetes Telefongerät modelliert. Das Zeilengerät kann über mehrere Adressen verfügen, wenn das modellierte Terminal mehr als eine Verzeichnisnummer (Directory Number, DN) unterstützt. Mehrere Aufrufdarstellungen auf demselben DN können als einzelne Adresse modelliert werden, die mehrere Aufrufe unterstützt.

Aufrufe zwischen zwei Stationen auf dem Switch verfügen über zwei Anrufhandles, von denen einer die Anrufansicht von der ersten Station (auf dem Leitungsgerät) und der andere die Anrufansicht von der zweiten Station (auf dem Leitungsgerät) ausgibt. Beispielsweise wird ein von einer Anwendung auf dem Server platzierter [**LineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) eines Drittanbieters an das Leitungsgerät weitergeleitet, das der Station zugeordnet ist, von der aus der Anruf gewählt werden soll. Ein Anrufhandle wird in dieser Zeile unter der in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) angegebenen Adresse erstellt (wodurch gesteuert wird, welcher DN auf einem Telefon verwendet wird, das mehrere DNs unterstützt). Wenn der Aufruf der Zieladresse angeboten wird, wird ein neues Aufrufhandle erstellt, das einen Aufruf im *Angebotszustand* anzeigt. -Anwendungen würden wissen, dass es sich um eine andere Ansicht desselben Aufrufs durch den **dwCallID-Member** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) handelte, die für beide Aufrufe gleich ist. Beide Aufrufe würden *sich im Leerlauf befinden,* wenn der Aufruf gelöscht wurde. Ein Aufruf kann aus der Drittanbieteranwendung gelöscht werden, indem ein [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) auf einem der Aufrufhandles erfolgt.

 

 



