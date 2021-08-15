---
title: Verwalten von Handles
description: Der Routingtabellen-Manager verwaltet einen Verweiszähler für alle informationen, die er verwaltet.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c701dbe8469baab54c427d42f9d603a976402ebb5693d1799989aeff74b65945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790603"
---
# <a name="managing-handles"></a>Verwalten von Handles

Der Routingtabellen-Manager verwaltet einen Verweiszähler für alle informationen, die er verwaltet. Dadurch wird verhindert, dass der Routingtabellen-Manager alle Freigegebenen Handles an den Arbeitsspeicher an einen Client zurückgibt. Jedes Mal, wenn ein Handle an den Aufrufer zurückgegeben wird, entweder als explizites Handle oder als Teil einer Informationsstruktur, z. B. [**RTM \_ DEST \_ INFO,**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info)wird die Verweisanzahl für das Objekt erhöht, das dem Handle entspricht. Wenn das Handle oder die Informationsstruktur freigegeben wird, wird der entsprechende Verweiszähler dekrementiert. Wenn der Verweiszähler 0 (null) wird, wird das Objekt freigegeben.

Die Funktionen [**RtmGetDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo) [**RtmGetEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo) [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) und [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) geben Informationsstrukturen zurück. Diese Funktionen entsprechen den Funktionen [**RtmReleaseDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo) [**RtmReleaseEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo) [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) und [**RtmRelaseNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

> [!Note]  
> Die [**RtmReleaseChangedDests-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) sollte verwendet werden, um Handles freizugeben, die durch einen Aufruf von [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)zurückgegeben wurden. Verwenden Sie [**rtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) nicht für geänderte Zielstrukturen.

 

Wenn ein Client ein bestimmtes Handle in einer Informationsstruktur beibehalten muss, während der Rest freigegeben wird, kann der Client [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) mit diesem Handle aufrufen, bevor die Informationsstruktur freigegeben wird. Das Handle kann dann durch einen Aufruf der Funktionen [**RtmReleaseDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo) [**RtmReleaseEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo) [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) und [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) freigegeben werden.

 

 




