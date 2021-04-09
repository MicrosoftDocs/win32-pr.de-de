---
description: IP-Hilfsprogramm bietet Funktionen zum Verwalten des Netzwerk Routings. Verwenden Sie die folgenden Funktionen zum Verwalten der IP-Routing Tabelle und zum Abrufen weiterer Routing Informationen.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Verwalten des Routings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862436"
---
# <a name="managing-routing"></a>Verwalten des Routings

IP-Hilfsprogramm bietet Funktionen zum Verwalten des Netzwerk Routings. Verwenden Sie die folgenden Funktionen zum Verwalten der IP-Routing Tabelle und zum Abrufen weiterer Routing Informationen.

Rufen Sie den Inhalt der IP-Routing Tabelle ab, indem Sie die [**getipforwardtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) -Funktion aufrufen. Bearbeiten Sie bestimmte Einträge in der IP-Routing Tabelle mithilfe der Funktionen " [**kreateipforwardentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry)", " [**deleteipforwardentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)" und " [**stipforwardentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) ". Verwenden Sie die Funktion " **kreateipforwardentry** ", um einen neuen Routing Tabelleneintrag hinzuzufügen. Verwenden Sie die **deleteipforwardentry** -Funktion, um einen vorhandenen Eintrag zu entfernen. Die Funktion " **settipforwardentry** " ändert einen vorhandenen Eintrag.

Mithilfe der routerverwaltungsfunktionen von IP Helper können Informationen darüber abgerufen werden, wie Datagramme über das Netzwerk weitergeleitet werden. Die [**getbestroute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) -Funktion Ruft die beste Route an eine angegebene Zieladresse ab. Die [**getbestinterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) -Funktion Ruft den Index der-Schnittstelle ab, die von der optimalen Route zu einer angegebenen Zieladresse verwendet wird. Schließlich ruft die [**getrttandhopcount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) -Funktion die Roundtripzeit (RTT) und die Anzahl der Hops an eine angegebene Zieladresse ab.

 

 



