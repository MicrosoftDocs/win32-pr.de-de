---
title: Registrieren einer SNMP-Agent-Anwendung
description: Zusätzlich zu den SNMP-Manager-Vorgängen unterstützt die WinSNMP-API-Version 2,0 auch SNMP-Agent-Vorgänge.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947891"
---
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="281e7-103">Registrieren einer SNMP-Agent-Anwendung</span><span class="sxs-lookup"><span data-stu-id="281e7-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="281e7-104">Zusätzlich zu den SNMP-Manager-Vorgängen unterstützt die WinSNMP-API-Version 2,0 auch SNMP-Agent-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="281e7-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="281e7-105">Um eine WinSNMP-Anwendung als SNMP-Agent zu registrieren, kann die Anwendung die [**snmpl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) abrufen.</span><span class="sxs-lookup"><span data-stu-id="281e7-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="281e7-106">Diese Funktion informiert die Microsoft WinSNMP-Implementierung, dass eine SNMP-Entität in der Rolle eines SNMP-Agents fungiert.</span><span class="sxs-lookup"><span data-stu-id="281e7-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="281e7-107">Die Anwendung kann auch **snmplauschen** aufzurufen, um die Implementierung zu informieren, wenn Sie nicht mehr als Agent fungiert.</span><span class="sxs-lookup"><span data-stu-id="281e7-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="281e7-108">Wenn eine Anwendung die [**snmpabhör**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) -Funktion aufruft und den Wert "Snmpapi" \_ im *lstatus* -Parameter übergibt, treten die folgenden Aktionen auf:</span><span class="sxs-lookup"><span data-stu-id="281e7-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="281e7-109">Die Entität, die in einer SNMP-agentrolle funktioniert, bindet Sie an ihren zugewiesenen Port und lauscht auf eingehende SNMP-Nachrichten Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="281e7-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="281e7-110">Der Agent verwendet anwendungsspezifische Logik, um jede SNMP-Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="281e7-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="281e7-111">Der Agent bildet geeignete Antworten auf die einzelnen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="281e7-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="281e7-112">Der Agent überträgt die Antwort an die anfordernde Entität, indem er die [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="281e7-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="281e7-113">Wenn der Agent **snmpsendmsg** aufruft, gibt er die Adresse des Agents im *srcentity* -Parameter und die Adresse der Remote-Manager-Entität im *dstentity* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="281e7-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="281e7-114">(Diese Werte sind das Gegenteil der Werte, die die agententität in diesen Parametern erhalten hat, als die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion zum Abrufen einer SNMP-Anforderung aufgerufen wurde.)</span><span class="sxs-lookup"><span data-stu-id="281e7-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="281e7-115">Weitere Informationen zu SNMP-Verwaltungs Anwendungen und-Agent-Anwendungen finden Sie unter [Informationen zu SNMP](about-snmp.md).</span><span class="sxs-lookup"><span data-stu-id="281e7-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




