---
title: Bewährte Methoden für den Lastenausgleich
description: Bewährte Methoden für den Lastenausgleich
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe4af9dffe758c89d1a494d4cc2597e057c563ca8c85db87d789ae91b89698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928595"
---
# <a name="load-balancing-best-practices"></a>Bewährte Methoden für den Lastenausgleich

Beim Einrichten und Konfigurieren des RPC-Lastenausgleichs sollten mehrere bewährte Methoden befolgt werden.

Zunächst sollte die Sicherheit für eingehende und ausgehende LBS-Aufrufe festgelegt werden. Dies bedeutet, dass beide optionalen [NoSecurity-Registrierungsschlüssel](configuring-load-balancing.md) entweder nicht vorhanden sein oder auf 0 (null) festgelegt werden sollten.

Zweitens muss die Front-End-Lastenausgleichslösung, die in Verbindung mit der RPC-Lastenausgleichslösung verwendet wird, besondere Aufmerksamkeit erhalten. Wenn der Front-End-Lastenausgleich beispielsweise einen einfachen Roundrobin-Lastenausgleich verwendet, sollte eine ungerade Anzahl von Servern in der Serverfarm vorhanden sein. Dadurch soll die Möglichkeit verringert werden, dass alle Verbindungen weitergeleitet und somit vom gleichen Server oder von denselben Servern verarbeitet werden.

Aus Sicherheitsgründen ist es in der Regel wünschenswert, dass eine Firewall den Zugriff auf RPC-Proxyserver kontrolliert. Wenn eine portbasierte Firewalllösung verwendet wird, müssen RPC-Endpunkte statisch sein, um die Anzahl der Ports zu begrenzen, die in der Firewall geöffnet sind. Auf Windows Server 2008 und höher von Windows stellt RPC einen Mechanismus zum Zuweisen eines statischen Ports zu dynamischen Endpunkten zur Verfügung. Dies wird durch die RPC-Netsh-Firewallbefehle erreicht. Ein Beispiel für einen Befehlssatz zum Festlegen der LBS-Schnittstelle auf den statischen Port 3010 ist:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

Mit dem RPC-Befehl netsh kann ein statischer Endpunkt für jede dynamische oder statische Schnittstelle festgelegt werden. Dies ist nützlich, wenn der Zugriff auf einen Computer eingeschränkt wird, auf dem eine portbasierte Firewalllösung ausgeführt wird. Wenn die Windows Firewalllösung verwendet wird, kann die RPC-Schnittstelle blockiert oder aktiviert werden, ohne sie einem bestimmten Port zuweisen zu müssen. Weitere Informationen finden Sie in der [RPC Netsh Firewall-Befehlsreferenz.](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10))

 

 