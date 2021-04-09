---
title: Verwalten von Handles
description: Der Routing Tabellen-Manager verwaltet einen Verweis Zähler für alle Informationen, die er verwaltet.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947810"
---
# <a name="managing-handles"></a>Verwalten von Handles

Der Routing Tabellen-Manager verwaltet einen Verweis Zähler für alle Informationen, die er verwaltet. Dadurch wird verhindert, dass der Routing Tabellen-Manager an einen Client alle Handles für den Arbeitsspeicher zurückgibt, der freigegeben wurde. Jedes Mal, wenn ein Handle an den Aufrufer zurückgegeben wird, entweder als explizites handle oder als Teil einer Informationsstruktur, wie z. [**b. RTM \_ dest \_ Info**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info), wird der Verweis Zähler für das Objekt, das dem Handle entspricht, inkrementiert. Wenn das Handle oder die Informationsstruktur freigegeben wird, wird der entsprechende Verweis Zähler verringert. Wenn der Verweis Zähler Null wird, wird das-Objekt freigegeben.

Die Funktionen [**rtmgetdestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**rtmgetentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**rtmgetrouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) und [**rtmgetnexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) geben Informationsstrukturen zurück. Diese Funktionen entsprechen den Funktionen [**rtmreleasedestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**rtmreleaseentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**rtmreleaserouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) und [**rtmrelasenexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

> [!Note]  
> Die [**rtmreleasechangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) -Funktion sollte verwendet werden, um Handles freizugeben, die durch einen [**rtmgetchangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)-aufrufswert zurückgegeben wurden. Verwenden Sie [**rtmreleasedests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) nicht für geänderte Zielstrukturen.

 

Wenn ein Client einen bestimmten Handle in einer Informationsstruktur aufbewahren muss, während er den Rest freigibt, kann der Client [**rtmreferencehandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) mit diesem Handle vor dem Freigeben der Informationsstruktur abrufen. Das Handle kann dann durch einen aufrufsbefehl der Funktionen [**rtmreleasedestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**rtmreleaseentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**rtmreleaserouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) und [**rtmrelasenexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) freigegeben werden.

 

 




