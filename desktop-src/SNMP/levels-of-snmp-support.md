---
title: Ebenen der SNMP-Unterstützung
description: Die Microsoft WinSNMP-Implementierung bietet SNMP-Kommunikationsunterstützung auf Ebene 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100635"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="39a4a-103">Ebenen der SNMP-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="39a4a-103">Levels of SNMP Support</span></span>

<span data-ttu-id="39a4a-104">Die Microsoft WinSNMP-Implementierung bietet SNMP-Kommunikationsunterstützung auf Ebene 2.</span><span class="sxs-lookup"><span data-stu-id="39a4a-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="39a4a-105">Ebene 2 unterstützt das IETF (Internet Engineering Task Force)-Standard-SNMPv2-Protokoll, wie in RFCs 1902-1908 definiert.</span><span class="sxs-lookup"><span data-stu-id="39a4a-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="39a4a-106">Außerdem wird der in RFC 1901 (SNMPv2C) definierte Community-basierte Nachrichten Wrapper unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39a4a-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="39a4a-107">Die Kommunikationsunterstützung auf Ebene 2 umfasst Nachrichten Codierungs-und Decodierungs Dienste, die zuvor in WinSNMP, Version 1.1 a, Unterstützung für die Ebene 0</span><span class="sxs-lookup"><span data-stu-id="39a4a-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="39a4a-108">Ebene 2 unterstützt auch alle SNMPv1-Protokoll Vorgänge, die zuvor in WinSNMP Version 1.1 a als Unterstützung für die Unterstützung von Ebene 1 bezeichnet wurden</span><span class="sxs-lookup"><span data-stu-id="39a4a-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="39a4a-109">Die-Implementierung gibt die maximale Ebene der SNMP-Kommunikation zurück, die Sie als Reaktion auf einen-Rückruf von der WinSNMP-Anwendung an die [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39a4a-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="39a4a-110">Wenn die WinSNMP-Anwendung die Implementierung nur für die SNMP-Nachrichten Codierung und-Decodierung verwendet, muss die Anwendung erforderliche Transformationen durchführen, die von der Implementierung durchgeführt worden wären.</span><span class="sxs-lookup"><span data-stu-id="39a4a-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="39a4a-111">Dies schließt das Übersetzen von SNMPv1 Traps ein, die von einem Rückruf der [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion zurückgegeben werden, in SNMPv2C Traps.</span><span class="sxs-lookup"><span data-stu-id="39a4a-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="39a4a-112">Es umfasst auch das Übersetzen von durch SNMPv1 definierten PDU-Typen in den entsprechenden PDU-Typ, der in Übereinstimmung mit RFC 1908 durch SNMPv2C definiert ist.</span><span class="sxs-lookup"><span data-stu-id="39a4a-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




