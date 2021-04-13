---
title: Senden von SNMP-Nachrichten
description: Eine WinSNMP-Anwendung initiiert eine Übertragungs Anforderung durch Senden einer SNMP-Nachricht. SNMP-Nachrichten enthalten eine SNMP-Protokolldaten Einheit. Weitere Informationen finden Sie unter Arbeiten mit Protokolldaten Einheiten.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310715"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="77e37-105">Senden von SNMP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="77e37-105">Sending SNMP Messages</span></span>

<span data-ttu-id="77e37-106">Eine WinSNMP-Anwendung initiiert eine Übertragungs Anforderung durch Senden einer SNMP-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="77e37-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="77e37-107">SNMP-Nachrichten enthalten eine SNMP-Protokolldaten Einheit.</span><span class="sxs-lookup"><span data-stu-id="77e37-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="77e37-108">Weitere Informationen finden Sie unter [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="77e37-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="77e37-109">Eine WinSNMP-Anwendung muss die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) anrufen, um anzufordern, dass die Microsoft WinSNMP-Implementierung das PDU mit den anderen erforderlichen Nachrichten Elementen überträgt, die von der entsprechenden RFC definiert werden.</span><span class="sxs-lookup"><span data-stu-id="77e37-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="77e37-110">Neben der Ziel Entität muss die Anwendung die Quell Entität und einen Kontext für die Anforderung angeben.</span><span class="sxs-lookup"><span data-stu-id="77e37-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="77e37-111">Die [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77e37-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="77e37-112">Die Anwendung WinSNMP muss die Funktion [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) aufrufen, um die Antwort auf eine **snmpsendmsg** -Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="77e37-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="77e37-113">Die-Implementierung überprüft die Gültigkeit des PDU-und der anderen Message-Elemente, wenn eine Anwendung [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)aufruft.</span><span class="sxs-lookup"><span data-stu-id="77e37-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




