---
title: Konfigurieren von RPC für SPX/IPX
description: Bei Verwendung der ncacn \_ -SPX-und ncadg- \_ IPX-Transporte ist der Servername genau mit dem Servernamen unter Windows identisch.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471508"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="ae630-103">Konfigurieren von RPC für SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="ae630-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="ae630-104">Bei Verwendung der **ncacn- \_ SPX** -und **ncadg- \_ IPX** -Transporte ist der Servername genau mit dem Servernamen unter Windows identisch.</span><span class="sxs-lookup"><span data-stu-id="ae630-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="ae630-105">Da die Namen jedoch mithilfe von Novell-Protokollen verteilt werden, müssen Sie den Novell-Benennungs Konventionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ae630-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="ae630-106">Wenn es sich bei einem Servernamen nicht um einen gültigen Novell-Namen handelt, können Server mit den **ncacn- \_ SPX** -oder **ncadg- \_ IPX** -Transporten keine Endpunkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae630-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="ae630-107">Ein gültiger Novell-Servername enthält nur die Zeichen zwischen 0x20 und 0x7F.</span><span class="sxs-lookup"><span data-stu-id="ae630-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="ae630-108">Kleinbuchstaben werden in Großbuchstaben geändert.</span><span class="sxs-lookup"><span data-stu-id="ae630-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="ae630-109">Die folgenden Zeichen können nicht verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ae630-109">The following characters cannot be used:</span></span>

<span data-ttu-id="ae630-110">" \* ,./:; <=>?\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="ae630-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="ae630-111">Um die Kompatibilität mit der ersten Version von Windows NT zu gewährleisten, können Sie mit **ncacn \_ SPX** und **ncadg \_ IPX** auch ein spezielles Format des Server namens verwenden, der als Tilde-Name bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ae630-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="ae630-112">Der Tilde-Name besteht aus einer Tilde (~), gefolgt von der achtstelligen Netzwerk Nummer des Servers und gefolgt von der 12-stelligen Ethernet-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ae630-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="ae630-113">Tilde-Namen haben einen Vorteil, dass keine Namensdienst Funktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ae630-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="ae630-114">Wenn Sie also mit einem Server verbunden sind, funktioniert der Tilde-Name.</span><span class="sxs-lookup"><span data-stu-id="ae630-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="ae630-115">Die folgenden Tabellen enthalten zwei Beispielkonfigurationen, die die zuvor beschriebenen Punkte veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="ae630-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="ae630-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="ae630-116">Component</span></span>                            | <span data-ttu-id="ae630-117">Konfiguriert als</span><span class="sxs-lookup"><span data-stu-id="ae630-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="ae630-118">Windows-Server</span><span class="sxs-lookup"><span data-stu-id="ae630-118">Windows server</span></span>                       | <span data-ttu-id="ae630-119">NWCS</span><span class="sxs-lookup"><span data-stu-id="ae630-119">NWCS</span></span>               |
| <span data-ttu-id="ae630-120">Windows-Client</span><span class="sxs-lookup"><span data-stu-id="ae630-120">Windows client</span></span>                       | <span data-ttu-id="ae630-121">NWCS</span><span class="sxs-lookup"><span data-stu-id="ae630-121">NWCS</span></span>               |
| <span data-ttu-id="ae630-122">16-Bit-Windows-Client, MS-DOS-Client</span><span class="sxs-lookup"><span data-stu-id="ae630-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="ae630-123">NetWare-Redirector</span><span class="sxs-lookup"><span data-stu-id="ae630-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="ae630-124">Für die Konfiguration in der vorherigen Tabelle ist es erforderlich, dass Sie über NetWare-Dateiserver oder Router im Netzwerk verfügen.</span><span class="sxs-lookup"><span data-stu-id="ae630-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="ae630-125">Dies führt zu einer optimalen Leistung, da die Servernamen in der NetWare Bindery gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ae630-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="ae630-126">Komponente</span><span class="sxs-lookup"><span data-stu-id="ae630-126">Component</span></span>                            | <span data-ttu-id="ae630-127">Konfiguriert als</span><span class="sxs-lookup"><span data-stu-id="ae630-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="ae630-128">Windows-Server</span><span class="sxs-lookup"><span data-stu-id="ae630-128">Windows server</span></span>                       | <span data-ttu-id="ae630-129">SAP-Agent</span><span class="sxs-lookup"><span data-stu-id="ae630-129">SAP Agent</span></span>     |
| <span data-ttu-id="ae630-130">Windows-Client</span><span class="sxs-lookup"><span data-stu-id="ae630-130">Windows client</span></span>                       | <span data-ttu-id="ae630-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="ae630-131">IPX/SPX</span></span>       |
| <span data-ttu-id="ae630-132">16-Bit-Windows-Client, MS-DOS-Client</span><span class="sxs-lookup"><span data-stu-id="ae630-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="ae630-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="ae630-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="ae630-134">Die zweite Konfiguration funktioniert in einer Umgebung, die keine NetWare-Dateiserver oder-Router enthält (z. b. ein Netzwerk mit zwei Computern: ein Windows-Server und ein MS-DOS-Client).</span><span class="sxs-lookup"><span data-stu-id="ae630-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="ae630-135">Die Namensauflösung, die während des ersten Aufrufens eines Bindungs Handles erreicht wird, ist etwas langsamer als bei der ersten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae630-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="ae630-136">Außerdem führt die zweite Konfiguration zu mehr Datenverkehr, der über das Netzwerk generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ae630-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="ae630-137">Wenn ein RPC-Server einen SPX-oder IPX-Endpunkt verwendet, werden der Servername und der Endpunkt als Dienst Ankündigungs Protokoll (SAP-Server) vom Typ 640 (hexadezimal) registriert, um die Namensauflösung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ae630-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="ae630-138">Zum Auflösen eines Server namens sendet der RPC-Client eine SAP-Anforderung für alle Dienste desselben Typs und scannt dann die Liste der Antworten auf den Namen des Servers.</span><span class="sxs-lookup"><span data-stu-id="ae630-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="ae630-139">Dieser Prozess tritt während des ersten RPC-Aufrufs über die einzelnen Bindungs Handles auf.</span><span class="sxs-lookup"><span data-stu-id="ae630-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="ae630-140">Weitere Informationen zum SAP-Protokoll für Novell finden Sie in der NetWare-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ae630-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="ae630-141">Die 16-Bit-Windows-Client Anwendungen, die die **ncacn- \_ SPX** -oder **ncadg- \_ IPX** -Transporte verwenden, erfordern, dass die Datei installiert Nwipxspx.dll, um unter dem wow-Subsystem ausgeführt werden zu können.</span><span class="sxs-lookup"><span data-stu-id="ae630-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="ae630-142">Wenden Sie sich an Novell, um diese Datei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae630-142">Contact Novell to obtain this file.</span></span>

 

 

 




