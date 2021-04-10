---
title: Netzwerk Transport Fehler
description: Die Microsoft WinSNMP-Implementierung kann einen Netzwerk Transport Fehler erkennen, nachdem eine SNMP-Nachricht übermittelt wurde.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858411"
---
# <a name="network-transport-errors"></a><span data-ttu-id="f5c08-103">Netzwerk Transport Fehler</span><span class="sxs-lookup"><span data-stu-id="f5c08-103">Network Transport Errors</span></span>

<span data-ttu-id="f5c08-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f5c08-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f5c08-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f5c08-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f5c08-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="f5c08-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="f5c08-107">Die Microsoft WinSNMP-Implementierung kann einen Netzwerk Transport Fehler erkennen, nachdem eine SNMP-Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5c08-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="f5c08-108">In diesem Fall sendet die-Implementierung eine Daten Empfangs Benachrichtigung an die WinSNMP-Sitzung, die die Kommunikations Anforderung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="f5c08-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="f5c08-109">Die-Implementierung gibt beim \_ nächsten Aufrufe der [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion für die Sitzung auch einen Snmpapi-Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f5c08-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="f5c08-110">Die **snmprecvmsg** -Funktion schlägt mit einem erweiterten Fehlercode fehl, der auf einen Fehler in der Netzwerk Transportschicht hinweist.</span><span class="sxs-lookup"><span data-stu-id="f5c08-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="f5c08-111">Eine Liste der spezifischen Fehler auf der Transportschicht finden Sie auf den Referenzseiten für die Funktionen " [**snmpregiester**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)", " [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)" und " [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) ".</span><span class="sxs-lookup"><span data-stu-id="f5c08-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 