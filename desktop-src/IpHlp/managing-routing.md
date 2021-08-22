---
description: Das IP-Hilfsdienst bietet Features zum Verwalten des Netzwerkroutings. Verwenden Sie die folgenden Funktionen, um die IP-Routingtabelle zu verwalten und andere Routinginformationen zu erhalten.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Verwalten des Routings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3b351882e08be3d09615acd033e0fb86192aee8675e8f52c4812a1eba398ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146643"
---
# <a name="managing-routing"></a>Verwalten des Routings

Das IP-Hilfsdienst bietet Features zum Verwalten des Netzwerkroutings. Verwenden Sie die folgenden Funktionen, um die IP-Routingtabelle zu verwalten und andere Routinginformationen zu erhalten.

Rufen Sie den Inhalt der IP-Routingtabelle ab, indem Sie die [**GetIpForwardTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) aufrufen. Bearbeiten Sie bestimmte Einträge in der IP-Routingtabelle mithilfe der Funktionen [**CreateIpForwardEntry,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry) [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)und [**SetIpForwardEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) Verwenden Sie **die CreateIpForwardEntry-Funktion,** um einen neuen Routingtabelleneintrag hinzuzufügen. Verwenden Sie **die DeleteIpForwardEntry-Funktion,** um einen vorhandenen Eintrag zu entfernen. Die **SetIpForwardEntry-Funktion** ändert einen vorhandenen Eintrag.

Die Routerverwaltungsfunktionen des IP-Hilfsprogramm können verwendet werden, um Informationen darüber abzurufen, wie Datagramme über das Netzwerk geroutet werden. Die [**GetBestRoute-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) ruft die beste Route zu einer angegebenen Zieladresse ab. Die [**GetBestInterface-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) ruft den Index der Schnittstelle ab, die von der besten Route zu einer angegebenen Zieladresse verwendet wird. Schließlich ruft die [**GetRTTAndHopCount-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) die Roundtripzeit (Roundtrip Time, RTT) und die Anzahl von Hops an eine angegebene Zieladresse ab.

 

 



