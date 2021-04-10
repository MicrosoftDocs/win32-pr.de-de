---
title: Verwalten von Traps und Benachrichtigungen
description: Die WinSNMP-Anwendung muss registriert werden, um Traps und Benachrichtigungen zu empfangen, indem die SnmpRegister-Funktion mit Snmpapi auf aufgerufen wird \_ . Die Anwendung kann die Registrierung und die Deaktivierung von Traps und Benachrichtigungen aufheben, indem Sie die-Funktion mit Snmpapi \_ Off aufrufen.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856632"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="91019-104">Verwalten von Traps und Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="91019-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="91019-105">Die WinSNMP-Anwendung muss registriert werden, um Traps und Benachrichtigungen zu empfangen, indem die [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) -Funktion mit Snmpapi auf aufgerufen wird \_ .</span><span class="sxs-lookup"><span data-stu-id="91019-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="91019-106">Die Anwendung kann die Registrierung und die Deaktivierung von Traps und Benachrichtigungen aufheben, indem Sie die-Funktion mit Snmpapi \_ Off aufrufen.</span><span class="sxs-lookup"><span data-stu-id="91019-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="91019-107">Wenn die Anwendung **snmpregiester** aufruft, stehen mehrere Optionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="91019-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="91019-108">Die Anwendung kann sich für die folgenden Traps und Benachrichtigungen registrieren oder die Registrierung aufheben:</span><span class="sxs-lookup"><span data-stu-id="91019-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="91019-109">Ein Typ von Trap oder Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="91019-109">One type of trap or notification</span></span>
-   <span data-ttu-id="91019-110">Alle Traps und Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="91019-110">All traps and notifications</span></span>
-   <span data-ttu-id="91019-111">Alle Quellen von Trap-und Benachrichtigungs Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91019-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="91019-112">Traps und Benachrichtigungen von allen Verwaltungs Entitäten</span><span class="sxs-lookup"><span data-stu-id="91019-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="91019-113">Traps und Benachrichtigungen für jeden Kontext</span><span class="sxs-lookup"><span data-stu-id="91019-113">Traps and notifications for every context</span></span>

<span data-ttu-id="91019-114">Zum Registrieren und Empfangen eines vordefinierten Traps oder Benachrichtigungs Typs muss die Anwendung für jeden vordefinierten Typ einen Objekt Bezeichner (eine [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur) definieren.</span><span class="sxs-lookup"><span data-stu-id="91019-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="91019-115">Die-Struktur muss eine Muster Vergleichs Sequenz für den Typ von Trap oder Benachrichtigung enthalten.</span><span class="sxs-lookup"><span data-stu-id="91019-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="91019-116">RFC 1907, "Verwaltungs Informationsbasis für Version 2 des Simple Network Management-Protokolls (SNMPv2)", definiert Trap-und Benachrichtigungs Objekt-IDs.</span><span class="sxs-lookup"><span data-stu-id="91019-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="91019-117">Zum Abrufen von ausstehenden Trap Daten und Benachrichtigungen für eine WinSNMP-Sitzung muss eine WinSNMP-Anwendung die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion mit dem Sitzungs handle aufrufen, das von der [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="91019-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="91019-118">Weitere Informationen finden Sie unter [Senden von SNMP-Nachrichten](sending-snmp-messages.md) und [empfangen von SNMP-Nachrichten](receiving-snmp-messages.md).</span><span class="sxs-lookup"><span data-stu-id="91019-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="91019-119">Weitere Informationen zur Zuordnung und Aufhebung der Zuordnung von Ressourcen für Traps und Benachrichtigungen finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="91019-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




