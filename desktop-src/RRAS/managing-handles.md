---
title: Verwalten von Handles
description: Der Routingtabellen-Manager verwaltet einen Verweiszähler für alle von ihm verwalteten Informationen.
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

Der Routingtabellen-Manager verwaltet einen Verweiszähler für alle von ihm verwalteten Informationen. Dadurch wird verhindert, dass der Routingtabellen-Manager alle Freihandles für den Arbeitsspeicher an einen Client zurückleiten kann. Jedes Mal, wenn ein Handle an den Aufrufer zurückgegeben wird, entweder als explizites Handle oder als Teil einer Informationsstruktur, z. B. [**RTM \_ DEST \_ INFO,**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info)wird die Verweisanzahl für das Objekt, das dem Handle entspricht, erhöht. Wenn das Handle oder die Informationsstruktur freigegeben wird, wird die entsprechende Verweisanzahl dekrementiert. Wenn der Verweiszähler null wird, wird das -Objekt frei.

Die [**Funktionen RtmGetDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo) [**RtmGetEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo) [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) und [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) geben Informationsstrukturen zurück. Diese Funktionen entsprechen [**den Funktionen RtmReleaseDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo) [**RtmReleaseEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo) [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) bzw. [**RtmRelaseNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

> [!Note]  
> Die [**RtmReleaseChangedDests-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) sollte verwendet werden, um Handles frei zu geben, die durch einen Aufruf von [**RtmGetChangedDests zurückgegeben wurden.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) Verwenden Sie [**rtmReleaseDests nicht für geänderte**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) Zielstrukturen.

 

Wenn ein Client während der Freigabe des Rests ein bestimmtes Handle in einer Informationsstruktur behalten muss, kann der Client [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) mit diesem Handle aufrufen, bevor er die Informationsstruktur frei gibt. Das Handle kann dann durch einen Aufruf der Funktionen [**RtmReleaseDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo) [**RtmReleaseEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo) [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) und [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) freigegeben werden.

 

 




