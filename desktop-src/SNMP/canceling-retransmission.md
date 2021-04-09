---
title: Neuübertragung wird abgebrochen
description: Wenn innerhalb des Timeout Zeitraums, der für eine Ziel Entität angegeben ist, keine Antwort auf eine Kommunikations Anforderung vorhanden ist, und wenn für die Entität reübertragungen angegeben werden, überträgt die Microsoft WinSNMP-Implementierung die Anforderung erneut.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036956"
---
# <a name="canceling-retransmission"></a><span data-ttu-id="3d95d-103">Neuübertragung wird abgebrochen</span><span class="sxs-lookup"><span data-stu-id="3d95d-103">Canceling Retransmission</span></span>

<span data-ttu-id="3d95d-104">Wenn innerhalb des Timeout Zeitraums, der für eine Ziel Entität angegeben ist, keine Antwort auf eine Kommunikations Anforderung vorhanden ist, und wenn für die Entität reübertragungen angegeben werden, überträgt die Microsoft WinSNMP-Implementierung die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="3d95d-104">If there is no response to a communication request within the time-out period specified for a destination entity, and if retransmissions are specified for the entity, the Microsoft WinSNMP implementation retransmits the request.</span></span> <span data-ttu-id="3d95d-105">Ein Aufrufe der [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) -Funktion kann diesen Neuübertragungs-Cycle abbrechen und interne Datenstrukturen freigeben, die der Nachrichten Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d95d-105">A call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function can cancel this retransmission cycle and release internal data structures associated with the message request.</span></span>

<span data-ttu-id="3d95d-106">Beachten Sie, dass es möglich ist, dass eine Ziel Entität eine SNMP-Nachricht empfängt, die durch einen Rückruf der [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) -Funktion abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="3d95d-106">Note that it is possible for a destination entity to receive an SNMP message that has been canceled by a call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function.</span></span> <span data-ttu-id="3d95d-107">Es ist auch möglich, dass eine Ziel Entität auf eine abgebrochene SNMP-Nachricht reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="3d95d-107">It is also possible that a destination entity can respond to a canceled SNMP message.</span></span> <span data-ttu-id="3d95d-108">Dies liegt daran, dass Transaktions Warteschlangen auf mehreren Ebenen auftreten.</span><span class="sxs-lookup"><span data-stu-id="3d95d-108">This is because transaction queuing occurs at multiple levels.</span></span> <span data-ttu-id="3d95d-109">Nachdem eine Nachricht jedoch durch einen Aufruf von [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)abgebrochen wurde, überträgt die Microsoft WinSNMP-Implementierung die Nachricht nicht erneut, sendet eine Antwort-PDU oder sendet eine Timeout Benachrichtigung an die Anwendung für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3d95d-109">However, once a message has been canceled by a call to [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), the Microsoft WinSNMP implementation will not retransmit the message, submit a response PDU, or send a time-out notification to the application for that message.</span></span>

 

 




