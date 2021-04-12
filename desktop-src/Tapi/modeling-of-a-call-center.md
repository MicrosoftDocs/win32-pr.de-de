---
description: Dienstanbieter können jede Ressource auf der PBX als Zeilen Gerät und möglicherweise ein zugeordnetes Telefongerät verfügbar machen.
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: Modellieren eines Callcenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393338"
---
# <a name="modeling-of-a-call-center"></a>Modellieren eines Callcenter

Dienstanbieter können jede Ressource auf der PBX als Zeilen Gerät und möglicherweise ein zugeordnetes Telefongerät verfügbar machen. Terminals, die mehrere Aufrufe unterstützen, würden dies über mehrere Adressen tun, ebenso wie in der erst Anbieter-Callcenter-Steuerung. Tatsächlich ist die Drittanbieter Ansicht eines Geräts identisch mit der Ansicht des ersten Anbieters. Anwendungen auf dem Server können alle Geräte von erst Anbietern sehen und Steuern, während ein einzelner Client-PC, der mit dem Server verbunden ist, nur die Geräte erkennen kann, die über die von tapisrv auf dem Server verwalteten Zugriffs Steuerungen sichtbar gemacht werden. Andere Ressourcen als Terminals können auch als Linien Geräte modelliert werden. Beispielsweise würde eine ACD-Warteschlange oder ein Routen Punkt als Linien Gerät modelliert werden, das viele aktive Aufrufe haben könnte. ein IVR-Server, ein sprach-e-Mail-Server oder ein Satz von vorher sagewähl Ports kann auch als Linien Gerät modelliert werden, das mehrere Aufrufe unterstützt.

Innerhalb dieses Modells können der Status des adressierten Geräts und der zugeordneten Aufrufe überwacht werden, auch wenn vorhandene TAPI-Nachrichten wie [**line \_ linedevstate**](line-linedevstate.md), [**line \_ addressstate**](line-addressstate.md), [**line \_ CallState**](line-callstate.md)und [**line \_ CallInfo**](line-callinfo.md)sowie Details durch Funktionen wie [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus), [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus), [**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)und [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)abgerufen werden. Wenn ein TAPI-Objekt über eine Anwendung eines Drittanbieters auf dem Server ausgeführt wird, ist das Ergebnis identisch mit dem, was passiert wäre, wenn das gleiche Objekt von einer Anwendung eines Drittanbieters, die auf einem Client Computer ausgeführt wird, der diesem Gerät zugeordnet ist, auf ähnliche Weise verarbeitet würde. Die vom Server Dienstanbieter gesendeten Status Hinweise, die das Wechsel-Fabric (oder den Switch) steuern, werden sowohl für Anwendungen, die auf dem Server ausgeführt werden, als auch für die, die auf zugeordneten autorisierten Clients

 

 



