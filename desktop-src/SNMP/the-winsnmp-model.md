---
title: Das WinSNMP-Modell
description: Das WinSNMP-kompatible Modell umfasst die folgenden grundlegenden Komponenten.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036618"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="52997-103">Das WinSNMP-Modell</span><span class="sxs-lookup"><span data-stu-id="52997-103">The WinSNMP Model</span></span>

<span data-ttu-id="52997-104">Das WinSNMP-kompatible Modell umfasst die folgenden grundlegenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="52997-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="52997-105">Eine mit WinSNMP aktivierte SNMP-Netzwerk Verwaltungs Anwendung, d. h. eine WinSNMP-kompatible *Anwendung*</span><span class="sxs-lookup"><span data-stu-id="52997-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="52997-106">Die WinSNMP-Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="52997-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="52997-107">Einen WinSNMP-aktivierten SNMP-Dienstanbieter, d. h. eine WinSNMP-kompatible *Implementierung*</span><span class="sxs-lookup"><span data-stu-id="52997-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="52997-108">Netzwerk Verwaltungs Anwendungen, die SNMP-Nachrichten vermitteln müssen, funktionieren effizient in einer ereignisgesteuerten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="52997-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="52997-109">Dies liegt daran, dass SNMP ein datagrammbasiertes oder verbindungsloses Protokoll zwischen Remote Entitäten ist, die keine virtuellen Verbindungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="52997-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="52997-110">Da Microsoft Windows-Anwendungen auch ereignisgesteuert sind, verwendet WinSNMP ein Programmiermodell, bei dem das empfangen und Verarbeiten von Anwendungen für die Verwaltung von asynchronen *Nachrichten Ereignissen* erfolgt.</span><span class="sxs-lookup"><span data-stu-id="52997-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="52997-111">Ein asynchrones Nachrichten Ereignis kann eine SNMP-Vorgangs Anforderung von einer Manager-Anwendung oder die Antwort auf eine Anforderung durch eine Agent-Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="52997-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="52997-112">SNMP sendet Anforderungen und Antworten als SNMP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="52997-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="52997-113">Eine SNMP-Nachricht ist eine SNMP-Protokolldaten Einheit (PDU) und zusätzliche Nachrichten Header Elemente, die durch die relevante RFC definiert werden.</span><span class="sxs-lookup"><span data-stu-id="52997-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="52997-114">Weitere Informationen finden Sie unter Informationen [zu SNMP-Nachrichten](about-snmp-messages.md), [Arbeiten mit Variablen Bindungs Listen](working-with-variable-binding-lists.md) und [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="52997-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 




