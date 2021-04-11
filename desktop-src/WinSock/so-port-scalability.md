---
description: Aktiviert die Skalierbarkeit des lokalen Ports für einen Socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129120"
---
# <a name="so_port_scalability"></a><span data-ttu-id="49cee-103">\_Port \_ Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="49cee-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="49cee-104">Die **Option \_ Port \_ Skalierbarkeits** Socket ermöglicht die lokale Port Skalierbarkeit für einen Socket.</span><span class="sxs-lookup"><span data-stu-id="49cee-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="49cee-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_Port \_ Skalierbarkeit**</span><span class="sxs-lookup"><span data-stu-id="49cee-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49cee-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="49cee-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="49cee-107">Die **Option \_ Port \_ Skalierbarkeits** -Socket ermöglicht die lokale Port Skalierbarkeit, indem die Zuordnung von Port Belegungen für unterschiedliche lokale Adress Port Paare auf einem lokalen Computer mehrfach zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="49cee-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49cee-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49cee-108">Remarks</span></span>

<span data-ttu-id="49cee-109">Hinweis: auf Plattformen, auf denen sowohl \_ \_ die Port Skalierbarkeit als auch \_ die Wiederverwendung von \_ unicastport unterstützt werden, bevorzugen Sie die Verwendung von " \_ \_ unicastport".</span><span class="sxs-lookup"><span data-stu-id="49cee-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="49cee-110">Proxy Serverumgebungen haben aufgrund eingeschränkter lokaler Port Verfügbarkeit Skalierbarkeits Probleme.</span><span class="sxs-lookup"><span data-stu-id="49cee-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="49cee-111">Eine Möglichkeit, dieses Problem zu umgehen, besteht darin, dem Computer weitere IP-Adressen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="49cee-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="49cee-112">Standardmäßig sind für die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion verwendete Platzhalter Anschlüsse jedoch auf die Größe des dynamischen Port Bereichs auf dem lokalen Computer beschränkt (bis zu 64K Ports, aber in der Regel weniger), unabhängig von der Anzahl der IP-Adressen auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="49cee-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="49cee-113">Um dies zu umgehen, muss die Anwendung ihren eigenen Port Pool entweder mit Port Reservierung oder mithilfe von Heuristik verwalten.</span><span class="sxs-lookup"><span data-stu-id="49cee-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="49cee-114">Um zu vermeiden, dass jede Anwendung, die Skalierbarkeit erfordert, einen eigenen Port Pool verwaltet und eine größere Skalierbarkeit ermöglicht, während die Anwendungs Kompatibilität gewahrt bleibt, wurde mit Windows Server 2008 die Socketoption " **\_ Port \_ Skalierbarkeit** " eingeführt, um die Platz Zuweisung von Platzhaltern zu maximieren</span><span class="sxs-lookup"><span data-stu-id="49cee-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="49cee-115">Die Port Zuordnung wird maximiert, indem es einer Anwendung ermöglicht, Platzhalter Anschlüsse für jede eindeutige lokale Adresse und jedes einzelne Port Paar zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="49cee-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="49cee-116">Wenn ein lokaler Computer also über vier IP-Adressen verfügt, können bis zu 256 k Platzhalter Anschlüsse (64 K-Ports × 4 IP-Adressen) durch Platzhalter [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Funktionsanforderungen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="49cee-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="49cee-117">Wenn die **Option \_ Port \_ Skalierbarkeits** -Socket für einen Socket festgelegt ist und ein Aufrufen der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion für eine angegebene Adresse und einen Platzhalter Anschluss erfolgt (der *Name* -Parameter wird mit einer bestimmten Adresse und dem Port 0 festgelegt), wird von Winsock ein Port für die angegebene Adresse zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="49cee-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="49cee-118">Diese Zuordnung basiert auf allen möglichen IP-Adressen und Ports/pro Adresse auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="49cee-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="49cee-119">Wenn ein Platzhalter Anschluss mithilfe der Option **" \_ Port \_ Skalierbarkeit** " abgerufen wird, kann dieser Port nicht von einem anderen Socket zugeordnet werden, ohne dass die Option " **\_ Port \_ Skalierbarkeit** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49cee-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="49cee-120">Diese Einschränkung ist vorhanden, um Probleme mit der Abwärtskompatibilität bei Anwendungen zu vermeiden, die davon ausgehen, dass ein Platzhalter lokaler Port nicht wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="49cee-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="49cee-121">Dies bedeutet, dass Anwendungen, die eine große Anzahl von Ports mithilfe der **\_ Port \_ Skalierbarkeit** abrufen, ältere Anwendungen von Ports verhungern können.</span><span class="sxs-lookup"><span data-stu-id="49cee-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="49cee-122">Wenn alle verfügbaren kurzlebigen Ports für mindestens eine Adresse mit der **\_ Port \_ Skalierbarkeit** abgerufen wurden, sind keine weiteren Platzhalter Port Zuordnungen ohne die Socketoption möglich.</span><span class="sxs-lookup"><span data-stu-id="49cee-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="49cee-123">Um einen Effekt zu haben, muss die Option **\_ Port \_ Skalierbarkeit** festgelegt werden, bevor die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="49cee-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="49cee-124">Ein Beispiel dafür, wie dies auf einem Computer mit zwei Adressen verwendet wird, ist im folgenden aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="49cee-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="49cee-125">Die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion wird von einem Prozess aufgerufen, um einen Socket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="49cee-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="49cee-126">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion wird aufgerufen, um die Option " **\_ Port \_ Skalierbarkeit** " für den neu erstellten Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="49cee-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="49cee-127">Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion wird aufgerufen, um eine Bindung für eine der IP-Adressen des lokalen Computers und Port 0 durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="49cee-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="49cee-128">Die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion wird dann aufgerufen, um eine Verbindung mit einer Remote-IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="49cee-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="49cee-129">Der Socket wird von der Anwendung nach Bedarf verwendet.</span><span class="sxs-lookup"><span data-stu-id="49cee-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="49cee-130">Eine [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) wird vom gleichen Prozess (möglicherweise einem anderen Thread) aufgerufen, um einen zweiten Socket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="49cee-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="49cee-131">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion wird aufgerufen, um die Option " **\_ Port \_ Skalierbarkeits** -Socket" für den neu erstellten zweiten Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="49cee-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="49cee-132">Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion wird mit der zweiten IP-Adresse des lokalen Computers und Port 0 aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="49cee-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="49cee-133">Auch wenn alle Ports zuvor zugeordnet wurden, ist dieser Vorgang erfolgreich, da auf dem lokalen Computer mehrere IP-Adressen verfügbar sind und die Option **\_ Port \_ Skalierbarkeits** -Socket für beide Sockets im gleichen Prozess festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="49cee-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="49cee-134">Die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion wird dann aufgerufen, um eine Verbindung mit einer Remote-IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="49cee-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="49cee-135">Der zweite Socket wird von der Anwendung nach Bedarf verwendet.</span><span class="sxs-lookup"><span data-stu-id="49cee-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cee-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49cee-136">Requirements</span></span>



| <span data-ttu-id="49cee-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49cee-137">Requirement</span></span> | <span data-ttu-id="49cee-138">Wert</span><span class="sxs-lookup"><span data-stu-id="49cee-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49cee-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49cee-139">Minimum supported client</span></span><br/> | <span data-ttu-id="49cee-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="49cee-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="49cee-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49cee-141">Minimum supported server</span></span><br/> | <span data-ttu-id="49cee-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49cee-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="49cee-143">Header</span><span class="sxs-lookup"><span data-stu-id="49cee-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cee-144"><dt>Ws2def. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cee-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cee-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49cee-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cee-146">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="49cee-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="49cee-147">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="49cee-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="49cee-148">**Optionen des Sol- \_ socketsockets**</span><span class="sxs-lookup"><span data-stu-id="49cee-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="49cee-149">**Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="49cee-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




