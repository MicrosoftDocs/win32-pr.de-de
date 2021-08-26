---
title: Abrufen von Informationen
description: RTMv2 ermöglicht einem Client das Abrufen der Informationen, auf die von einem angegebenen Handle verwiesen wird, mithilfe der Funktionen RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo und RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51958fccc8a07e8846705945d9210f4259dfd89b1e3cefccd65d57dd0f033757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028020"
---
# <a name="retrieving-information"></a>Abrufen von Informationen

RTMv2 ermöglicht einem Client das Abrufen der Informationen, auf die von einem angegebenen Handle verwiesen wird, mithilfe der Funktionen [**RtmGetEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo) [**RtmGetDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo) [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)und [**RtmGetNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

Diese Funktionsaufrufe verfügen über entsprechende Funktionen ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)), um die Handles freizugeben, die der vom Routingtabellen-Manager zurückgegebenen Informationsstruktur zugeordnet sind.

> [!Note]  
> Informationen für Clients sind nur in der aktuellen Instanz und Adressfamilie verfügbar.

 

Beispielcode, der zeigt, wie diese Funktionen verwendet werden, finden Sie unter [Suchen nach der besten Route.](search-for-the-best-route.md)

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Verwenden von RtmGetExactMatchRoute und RtmGetExactMatchDestination

Die Funktionen [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) und [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) werden von Clients verwendet, um eine bestimmte Route oder ein bestimmtes Ziel zu finden. Diese Funktionen sparen Zeit, indem sie die Vergleichsarbeit für den Client durchführen.

Wenn RIP beispielsweise eine Route aktualisiert, muss RIP die alten Metrikinformationen beibehalten. RIP sucht nach der Route und ihren Informationen. Dann kann RIP die Informationen kopieren und die Route aktualisieren.

## <a name="using-rtmgetmostspecificdestination"></a>Verwenden von RtmGetMostSpecificDestination

Die [**RtmGetMostSpecificDestination-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) wird verwendet, um das Ziel zu suchen, das dem angegebenen Netzwerkpräfix am besten entspricht.

Beispielsweise verwendet der Multicastgruppen-Manager diese Funktion, um eine Reversepfadweiterleitung (Reverse Path-Forwarding, RPF) für eine einzelne Adresse durchzuführen. Die Funktion kann auch verwendet werden, um den lokalen nächsten Hop für einen bestimmten nächsten Remotehop zu suchen.

Beispielcode, der zeigt, wie diese Funktionen verwendet werden, finden Sie unter [Suchen nach Routen mithilfe einer Präfixstruktur](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) und [Suchen nach der besten Route.](search-for-the-best-route.md)

## <a name="using-rtmgetlessspecificdestination"></a>Verwenden von RtmGetLessSpecificDestination

Die [**RtmGetLessSpecificDestination-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) wird verwendet, um das Ziel zu finden, das die nächstbeste Übereinstimmung für das angegebene Netzwerkpräfix ist. Diese Funktion kann wiederholt aufgerufen werden, um die nächste aufeinander folgende weniger spezifische Übereinstimmung zurückzugeben, bis keine weiteren Ziele übereinstimmen.

Diese Funktion wird nach einem Aufruf von [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)aufgerufen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Suchen nach Routen mithilfe einer Präfixstruktur.](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)

## <a name="using-rtmisbestroute"></a>Verwenden von RtmIsBestRoute

Mit der [**RtmIsBestRoute-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) kann ein Client schnell ermitteln, ob eine bestimmte Route die beste Route zu einem Ziel ist. Beispielsweise muss ein Client eine bestimmte Route möglicherweise nur speichern, wenn es sich um die beste Route handelt. Daher kann der Client diese Funktion aufrufen, anstatt alle Routen aufzurufen und den Vergleich selbst vorzunehmen.

 

 




