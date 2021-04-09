---
title: Bewährte Methoden für den Lastenausgleich
description: Bewährte Methoden für den Lastenausgleich
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948962"
---
# <a name="load-balancing-best-practices"></a>Bewährte Methoden für den Lastenausgleich

Beim Einrichten und Konfigurieren des RPC-Lasten Ausgleichs sollten einige bewährte Methoden befolgt werden.

Zuerst muss die Sicherheit bei eingehenden und ausgehenden lbs-aufrufen festgelegt werden. Dies bedeutet, dass beide optionalen [NoSecurity](configuring-load-balancing.md) -Registrierungsschlüssel entweder nicht vorhanden oder auf 0 (null) festgelegt werden sollen.

Zum anderen muss die Front-End-Lasten Ausgleichs Lösung, die in Verbindung mit der Lösung für den RPC-Lastenausgleich verwendet wird, berücksichtigt werden. Wenn beispielsweise der Front-End-Load Balancer einen einfachen Roundrobin-Lastenausgleich verwendet, sollte in der Serverfarm eine ungerade Anzahl von Servern vorhanden sein. Dadurch wird die Wahrscheinlichkeit verringert, dass alle Verbindungen weitergeleitet und somit von demselben Server oder Server gewartet werden.

Aus Sicherheitsgründen ist es in der Regel wünschenswert, dass eine Firewall den Zugriff auf RPC-Proxy Server steuert. Wenn eine Port basierte Firewalllösung verwendet wird, müssen die RPC-Endpunkte statisch sein, um die Anzahl der in der Firewall geöffneten Ports einzuschränken. Unter Windows Server 2008 und neueren Versionen von Windows bietet RPC einen Mechanismus zum Zuweisen eines statischen Ports zu dynamischen Endpunkten. Dies wird durch die RPC-Befehle netsh Firewall erreicht. Ein Beispielsatz von Befehlen zum Festlegen der lbs-Schnittstelle auf den statischen Port 3010 lautet wie folgt:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

Der RPC Netsh-Befehl kann verwendet werden, um einen statischen Endpunkt für eine beliebige dynamische oder statische Schnittstelle festzulegen. Dies ist nützlich, wenn der Zugriff auf einen Computer beschränkt wird, auf dem eine Port basierte Firewalllösung ausgeführt wird Wenn die Windows-Firewall-Lösung verwendet wird, kann die RPC-Schnittstelle blockiert oder aktiviert werden, ohne dass Sie einem bestimmten Port zugewiesen werden muss. Weitere Informationen finden Sie in der [RPC-Befehlsreferenz netsh Firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).

 

 