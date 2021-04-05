---
title: Empfangen von SNMP-Nachrichten
description: Die Anwendung WinSNMP muss die Funktion snmprecvmsg aufrufen, um die Antwort auf eine snmpsendmsg-Anforderung abzurufen.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713062"
---
# <a name="receiving-snmp-messages"></a><span data-ttu-id="39840-103">Empfangen von SNMP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="39840-103">Receiving SNMP Messages</span></span>

<span data-ttu-id="39840-104">Die Anwendung WinSNMP muss die Funktion [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) aufrufen, um die Antwort auf eine [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="39840-104">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request.</span></span>

<span data-ttu-id="39840-105">Die [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) -Funktion übergibt ein Anwendungsfenster Handle und einen Benachrichtigungs Bezeichner an die Microsoft WinSNMP-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="39840-105">The [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function passes an application window handle and a notification message identifier to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="39840-106">Wenn das Anwendungsfenster diese Nachricht empfängt, signalisiert es der Anwendung, die Funktion [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) mithilfe des Sitzungs Handles aufzurufen, das von [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="39840-106">When the application window receives this message, it signals the application to call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function using the session handle returned by [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span>

<span data-ttu-id="39840-107">Die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion gibt zwei Entitäts Handles, ein Kontext Handle und das Handle für ein PDU zurück.</span><span class="sxs-lookup"><span data-stu-id="39840-107">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function returns two entity handles, a context handle, and the handle to a PDU.</span></span> <span data-ttu-id="39840-108">Es wird empfohlen, dass die WinSNMP-Anwendung diese Ressourcen mit den Funktionen " [**snmpfreeentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)", " [**snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)" und " [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) " freigibt.</span><span class="sxs-lookup"><span data-stu-id="39840-108">It is recommended that the WinSNMP application free these resources using the [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) functions.</span></span>

<span data-ttu-id="39840-109">Weitere Informationen zum Verwalten der Zeit zwischen einem Aufruf der [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion und dem Empfang der entsprechenden Antwort finden Sie unter [Informationen zur erneuten Übertragung](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="39840-109">For additional information about managing the time between a call to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function and the receipt of the corresponding response, see [About Retransmission](about-retransmission.md).</span></span> <span data-ttu-id="39840-110">Weitere Informationen zur Verwendung des Felds **Request \_ ID** PDU zum Abgleichen einer Antwort-PDU mit der Anforderungs-PDU finden Sie unter [übereinstimmende Antwort und Anforderungs-PDUs](matching-response-and-request-pdus.md).</span><span class="sxs-lookup"><span data-stu-id="39840-110">For additional information about using the **request\_id** PDU field to match a response PDU with its request PDU, see [Matching Response and Request PDUs](matching-response-and-request-pdus.md).</span></span>

 

 




