---
title: Informationen zur Microsoft WinSNMP-Implementierung
description: Die Microsoft WinSNMP-Implementierung entspricht der WinSNMP-Version 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947309"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="0fa29-103">Informationen zur Microsoft WinSNMP-Implementierung</span><span class="sxs-lookup"><span data-stu-id="0fa29-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="0fa29-104">Die Microsoft WinSNMP-Implementierung entspricht der WinSNMP-Version 2,0.</span><span class="sxs-lookup"><span data-stu-id="0fa29-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="0fa29-105">Es werden alle Funktionen und Vorgänge unterstützt, die sowohl in der Version von WinSNMP, Version 1.1, als auch in den Nachtrag der WinSNMP-Version 2,0 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0fa29-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="0fa29-106">Die-Implementierung stellt die folgenden Dienste für WinSNMP-Anwendungen bereit:</span><span class="sxs-lookup"><span data-stu-id="0fa29-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="0fa29-107">Verwaltet die Kommunikation zu und von Verwaltungs Entitäten.</span><span class="sxs-lookup"><span data-stu-id="0fa29-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="0fa29-108">Die Entität kann sich auf dem lokalen Computer befinden oder über ein lokales oder weites Netzwerk oder über das Internet verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="0fa29-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="0fa29-109">Weitere Informationen finden Sie [Unterebenen der SNMP-Unterstützung](levels-of-snmp-support.md).</span><span class="sxs-lookup"><span data-stu-id="0fa29-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="0fa29-110">Blendet die Details des SNMP-Protokolls (Abstract Syntax Notation One, ASN. 1) und die grundlegenden Codierungsregeln (ber) zum Beschreiben der Übertragungs Syntax aus.</span><span class="sxs-lookup"><span data-stu-id="0fa29-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="0fa29-111">Überprüft die Richtigkeit von PDUs und lehnt ungültige PDUs ab.</span><span class="sxs-lookup"><span data-stu-id="0fa29-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="0fa29-112">Weitere Informationen finden Sie unter [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="0fa29-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="0fa29-113">Wandelt SNMPv2C PDU-Typen bei Bedarf in Übereinstimmung mit den entsprechenden RFCs um.</span><span class="sxs-lookup"><span data-stu-id="0fa29-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="0fa29-114">Konvertiert SNMPv1 Traps von einem SNMPv1-Agent in SNMPv2C Traps in Übereinstimmung mit RFC 1908, "Koexistenz zwischen Version 1 und Version 2 des Internet-Standard-Netzwerk Verwaltungs-Frameworks".</span><span class="sxs-lookup"><span data-stu-id="0fa29-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="0fa29-115">Weitere Informationen finden Sie unter Translation [Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span><span class="sxs-lookup"><span data-stu-id="0fa29-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="0fa29-116">Unterstützt die Neuübertragungs Richtlinie der Anwendung und bietet Unterstützung für die erneute Übertragungs Ausführung.</span><span class="sxs-lookup"><span data-stu-id="0fa29-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="0fa29-117">Weitere Informationen finden Sie in [der WinSNMP-Datenbank](the-winsnmp-database.md) und Informationen [zur erneuten Übertragung](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="0fa29-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="0fa29-118">Stellt Entitäts-und Kontext Übersetzungsunterstützung für die Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="0fa29-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="0fa29-119">Weitere Informationen finden Sie in [der WinSNMP-Datenbank](the-winsnmp-database.md) und [Festlegen des Entitäts-und Kontext Übersetzungsmodus](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="0fa29-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="0fa29-120">Weitere Informationen zur Beziehung zwischen einer WinSNMP-Anwendung und der-Implementierung finden Sie unter [WinSNMP-Datenverwaltung Konzepte](winsnmp-data-management-concepts.md) und [WinSNMP-Sitzungen](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="0fa29-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




