---
title: Abrufen von Informationen
description: RTMv2 ermöglicht einem Client das Abrufen der Informationen, auf die von einem bestimmten handle verwiesen wird, mithilfe der Funktionen rtmgetentityinfo, rtmgetdestinfo, rtmgetrouteinfo und rtmgetnexthopinfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206355"
---
# <a name="retrieving-information"></a>Abrufen von Informationen

RTMv2 ermöglicht einem Client das Abrufen der Informationen, auf die von einem bestimmten handle verwiesen wird, mithilfe der Funktionen [**rtmgetentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**rtmgetdestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**rtmgetrouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)und [**rtmgetnexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .

Diese Funktionsaufrufe verfügen über entsprechende Funktionen ([**rtmreleaseentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**rtmreleasedestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**rtmreleaserouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**rtmreleasenexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)), um die Handles freizugeben, die mit der vom Routing Tabellen-Manager zurückgegebenen Informationsstruktur verknüpft sind.

> [!Note]  
> Informationen für Clients sind nur in der aktuellen Instanz und Adressfamilie verfügbar.

 

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Suchen nach der besten Route](search-for-the-best-route.md).

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Verwenden von rtmgetexactmatchroute und rtmgetexactmatchdestination

Die Funktionen [**rtmgetexactmatchroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) und [**rtmgetexactmatchdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) werden von Clients verwendet, um eine bestimmte Route oder ein bestimmtes Ziel zu finden. Diese Funktionen sparen Zeit, indem Sie die vergleichsarbeit für den Client durcharbeiten.

Wenn z. b. RIP eine Route aktualisiert, muss RIP die alten metrikinformationen beibehalten. RIP sucht nach der Route und deren Informationen. Anschließend kann RIP die Informationen kopieren und die Route aktualisieren.

## <a name="using-rtmgetmostspecificdestination"></a>Verwenden von "rtmgetarstspecificdestination"

Mithilfe der Funktion [**rtmgetmuspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) wird das Ziel gefunden, das am besten mit dem angegebenen Netzwerk Präfix übereinstimmt.

Beispielsweise verwendet der Multicast-Gruppen-Manager diese Funktion, um eine RPF-Überprüfung (reversepfad-Weiterleitung) für eine einzelne Adresse auszuführen. Die-Funktion kann auch verwendet werden, um den lokalen nächsten Hop für einen bestimmten Remote-Hop zu suchen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie untersuchen nach Routen mithilfe eines Präfix Baums](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) und [Suchen nach der besten Route](search-for-the-best-route.md).

## <a name="using-rtmgetlessspecificdestination"></a>Verwenden von rtmgetlessspecificdestination

Die [**rtmgetlessspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) -Funktion wird verwendet, um das Ziel zu finden, das die nächstbeste Entsprechung für das angegebene Netzwerk Präfix ist. Diese Funktion kann wiederholt aufgerufen werden, um die nächste nachfolgende weniger spezifische Treffer Rückgabe zurückzugeben, bis keine weiteren Ziele mehr gefunden werden.

Diese Funktion wird nach einem Aufruf von [**rtmgetarstspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)aufgerufen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie untersuchen nach Routen mithilfe eines Präfix Baums](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Verwenden von rtmisbestroute

Die [**rtmisbestroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) -Funktion ermöglicht es einem Client, schnell herauszufinden, ob eine bestimmte Route die beste Route zu einem Ziel ist. Beispielsweise muss ein Client möglicherweise nur eine bestimmte Route speichern, wenn er die beste Route ist. Daher kann der Client diese Funktion anstelle von allen Routen auflisten und den Vergleich selbst durchführen.

 

 




