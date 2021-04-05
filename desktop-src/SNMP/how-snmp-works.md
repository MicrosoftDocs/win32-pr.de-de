---
title: Funktionsweise von SNMP
description: Gibt an, wie eine Anwendung der SNMP-Verwaltungskonsole von Drittanbietern Informationen aus dem SNMP-Dienst zurückgibt.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947575"
---
# <a name="how-snmp-works"></a><span data-ttu-id="31ee8-103">Funktionsweise von SNMP</span><span class="sxs-lookup"><span data-stu-id="31ee8-103">How SNMP Works</span></span>

<span data-ttu-id="31ee8-104">In den folgenden Schritten wird beschrieben, wie die SNMP-Verwaltungs Konsolenanwendung eines Drittanbieters Informationen aus dem SNMP-Dienst zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="31ee8-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="31ee8-105">Die SNMP-Verwaltungs Konsolenanwendung formuliert eine SNMP-Nachricht basierend auf der Eingabe des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="31ee8-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="31ee8-106">Die Meldung enthält eine Protokolldaten Einheit (PDU) und Authentifizierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="31ee8-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="31ee8-107">Die Verwaltungs Konsolenanwendung kann die Microsoft SNMP-Verwaltungs-API-Bibliothek (MGMTAPI.DLL) oder die Microsoft [WinSNMP-API](winsnmp-api.md) -Bibliothek (WSNMP32.DLL) verwenden, um diesen Schritt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="31ee8-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="31ee8-108">Die SNMP-Verwaltungs Konsolenanwendung sendet die SNMP-Nachricht mithilfe der SNMP-Dienst Bibliotheken an den SNMP-Dienst.</span><span class="sxs-lookup"><span data-stu-id="31ee8-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="31ee8-109">Der SNMP-Dienst empfängt die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="31ee8-109">The SNMP service receives the request.</span></span> <span data-ttu-id="31ee8-110">Dabei werden die Authentifizierungsinformationen und die Quell-IP-Adresse überprüft.</span><span class="sxs-lookup"><span data-stu-id="31ee8-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="31ee8-111">Der SNMP-Dienst wählt den geeigneten Erweiterungs-Agent aus und fordert an, dass der Agent die angeforderten Informationen abruft.</span><span class="sxs-lookup"><span data-stu-id="31ee8-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="31ee8-112">Der SNMP-Dienst sendet die Antwort an die Anwendung der SNMP-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="31ee8-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 




