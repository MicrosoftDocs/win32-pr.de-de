---
title: Informationen zu Traps und Benachrichtigungen
description: Eine Nachricht, die eine SNMP-Agent-Anwendung an eine WinSNMP-Anwendung senden kann, ist eine asynchrone Nachricht, die die Anwendung über ein wichtiges Ereignis informiert.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856192"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="852cd-103">Informationen zu Traps und Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="852cd-103">About Traps and Notifications</span></span>

<span data-ttu-id="852cd-104">Eine Nachricht, die eine SNMP-Agent-Anwendung an eine WinSNMP-Anwendung senden kann, ist eine asynchrone Nachricht, die die Anwendung über ein wichtiges Ereignis informiert.</span><span class="sxs-lookup"><span data-stu-id="852cd-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="852cd-105">Ein Beispiel für ein wichtiges Ereignis ist, wenn eine Netzwerkverbindung heruntergefahren wird oder wenn ein Authentifizierungsfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="852cd-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="852cd-106">Diese Nachrichten Typen werden unter SNMPv1 und Benachrichtigungen unter SNMPv2C als Traps bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="852cd-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="852cd-107">Die Microsoft WinSNMP-Implementierung übersetzt SNMPv1 Traps immer in das SNMPv2C-Format, wie in RFC 1908 definiert.</span><span class="sxs-lookup"><span data-stu-id="852cd-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="852cd-108">Wenn Sie die Funktion [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aufrufen, um ein Trap-PDU zu erstellen, können Sie nur ein SNMPv2C Trap-PDU erstellen.</span><span class="sxs-lookup"><span data-stu-id="852cd-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="852cd-109">Der einzige Typ von Trap-PDU, den Sie mit einem Aufrufen der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion aktualisieren können, ist ein SNMPv2C Trap-PDU.</span><span class="sxs-lookup"><span data-stu-id="852cd-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="852cd-110">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="852cd-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="852cd-111">Thema</span><span class="sxs-lookup"><span data-stu-id="852cd-111">Topic</span></span>                                                                                    | <span data-ttu-id="852cd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="852cd-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="852cd-113">Übersetzen von Traps von SNMPv1 in SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="852cd-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="852cd-114">Trap-Formate</span><span class="sxs-lookup"><span data-stu-id="852cd-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




