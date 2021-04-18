---
title: Aktivieren und Deaktivieren der erneuten Übertragung
description: Eine Anwendung kann den Modus für Neuübertragungen mit einem aufzurufenden Befehl der snmpsetretransmitmode-Funktion festlegen. Der neue Neuübertragungs Modus gilt für nachfolgende Aufrufe der snmpsendmsg-Funktion.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340418"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="c9d62-104">Aktivieren und Deaktivieren der erneuten Übertragung</span><span class="sxs-lookup"><span data-stu-id="c9d62-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="c9d62-105">Eine Anwendung kann den Modus für Neuübertragungen mit einem aufzurufenden Befehl der [**snmpsetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="c9d62-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="c9d62-106">Der neue Neuübertragungs Modus gilt für nachfolgende Aufrufe der [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c9d62-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="c9d62-107">Wenn die Anwendung **snmpsetretransmitmode** mit dem Neuübertragungs-Moduswert Snmpapi \_ on aufruft, beginnt die Microsoft WinSNMP-Implementierung mit der Ausführung der Neuübertragungs Richtlinie der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c9d62-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="c9d62-108">Der neue Modus für Neuübertragungen wirkt sich nicht auf ausstehende SNMP-Nachrichten aus.</span><span class="sxs-lookup"><span data-stu-id="c9d62-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="c9d62-109">Eine ausstehende Meldung ist eine Meldung, die zu dem Zeitpunkt, zu dem die Anwendung den Modus für die Neuübertragung ändert, keine Antwort hat.</span><span class="sxs-lookup"><span data-stu-id="c9d62-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="c9d62-110">Wenn die WinSNMP-Anwendung die [**snmpsetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) -Funktion mit dem Neuübertragungs-Moduswert Snmpapi \_ Off aufruft, beendet die-Implementierung die Ausführung der Richtlinie zum erneuten übertragen.</span><span class="sxs-lookup"><span data-stu-id="c9d62-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="c9d62-111">Die-Implementierung bricht Neuübertragungs Versuche für ausstehende SNMP-Nachrichten ab.</span><span class="sxs-lookup"><span data-stu-id="c9d62-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="c9d62-112">Dies liegt daran, dass es möglicherweise nicht möglich ist, dass die Implementierung alle ausstehenden SNMP-Anforderungen und-Vorgänge zuzüglich neuer Anforderungen verarbeitet, bevor ein Anwendungs Timeout oder ein Wiederholungsversuch ein Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="c9d62-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




