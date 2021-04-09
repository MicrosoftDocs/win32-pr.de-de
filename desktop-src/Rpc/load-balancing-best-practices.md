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
# <a name="load-balancing-best-practices"></a><span data-ttu-id="332ee-103">Bewährte Methoden für den Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="332ee-103">Load Balancing Best Practices</span></span>

<span data-ttu-id="332ee-104">Beim Einrichten und Konfigurieren des RPC-Lasten Ausgleichs sollten einige bewährte Methoden befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="332ee-104">Several best practices should be followed when setting up and configuring RPC Load balancing.</span></span>

<span data-ttu-id="332ee-105">Zuerst muss die Sicherheit bei eingehenden und ausgehenden lbs-aufrufen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="332ee-105">First, security should be set on incoming and outgoing LBS calls.</span></span> <span data-ttu-id="332ee-106">Dies bedeutet, dass beide optionalen [NoSecurity](configuring-load-balancing.md) -Registrierungsschlüssel entweder nicht vorhanden oder auf 0 (null) festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="332ee-106">This means both of the optional [NoSecurity](configuring-load-balancing.md) registry keys should either not be present or should be set to zero.</span></span>

<span data-ttu-id="332ee-107">Zum anderen muss die Front-End-Lasten Ausgleichs Lösung, die in Verbindung mit der Lösung für den RPC-Lastenausgleich verwendet wird, berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="332ee-107">Second, attention must be paid to the front end load balancing solution used in conjunction with the RPC Load Balancing solution.</span></span> <span data-ttu-id="332ee-108">Wenn beispielsweise der Front-End-Load Balancer einen einfachen Roundrobin-Lastenausgleich verwendet, sollte in der Serverfarm eine ungerade Anzahl von Servern vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="332ee-108">For example, if the front end load balancer uses simple round robin load balancing, an odd number of servers should exist in the server farm.</span></span> <span data-ttu-id="332ee-109">Dadurch wird die Wahrscheinlichkeit verringert, dass alle Verbindungen weitergeleitet und somit von demselben Server oder Server gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="332ee-109">This is to mitigate the possibility of all connections being forwarded and thus serviced by the same server or servers.</span></span>

<span data-ttu-id="332ee-110">Aus Sicherheitsgründen ist es in der Regel wünschenswert, dass eine Firewall den Zugriff auf RPC-Proxy Server steuert.</span><span class="sxs-lookup"><span data-stu-id="332ee-110">For security, it is commonly desirable to have a firewall control access to RPC Proxy servers.</span></span> <span data-ttu-id="332ee-111">Wenn eine Port basierte Firewalllösung verwendet wird, müssen die RPC-Endpunkte statisch sein, um die Anzahl der in der Firewall geöffneten Ports einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="332ee-111">If a port based firewall solution is employed, RPC endpoints must be static in order to limit the number of ports that are opened in the firewall.</span></span> <span data-ttu-id="332ee-112">Unter Windows Server 2008 und neueren Versionen von Windows bietet RPC einen Mechanismus zum Zuweisen eines statischen Ports zu dynamischen Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="332ee-112">On Windows Server 2008 and later versions of Windows, RPC provides a mechanism to assign a static port to dynamic endpoints.</span></span> <span data-ttu-id="332ee-113">Dies wird durch die RPC-Befehle netsh Firewall erreicht.</span><span class="sxs-lookup"><span data-stu-id="332ee-113">This is achieved through the RPC netsh firewall commands.</span></span> <span data-ttu-id="332ee-114">Ein Beispielsatz von Befehlen zum Festlegen der lbs-Schnittstelle auf den statischen Port 3010 lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="332ee-114">An example set of commands to set the LBS interface to the static port of 3010 is:</span></span>

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

<span data-ttu-id="332ee-115">Der RPC Netsh-Befehl kann verwendet werden, um einen statischen Endpunkt für eine beliebige dynamische oder statische Schnittstelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="332ee-115">The RPC netsh command can be used to set a static endpoint for any dynamic or static interface.</span></span> <span data-ttu-id="332ee-116">Dies ist nützlich, wenn der Zugriff auf einen Computer beschränkt wird, auf dem eine Port basierte Firewalllösung ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="332ee-116">This is useful when restricting access to a machine running a port based firewall solution.</span></span> <span data-ttu-id="332ee-117">Wenn die Windows-Firewall-Lösung verwendet wird, kann die RPC-Schnittstelle blockiert oder aktiviert werden, ohne dass Sie einem bestimmten Port zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="332ee-117">If the Windows firewall solution is used, the RPC interface can be blocked or enabled without having to assign it to a specific port.</span></span> <span data-ttu-id="332ee-118">Weitere Informationen finden Sie in der [RPC-Befehlsreferenz netsh Firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="332ee-118">For more information, see the [RPC netsh firewall command reference](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span></span>

 

 