---
title: WinSNMP-API
description: Mit der Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (der WinSNMP-API) Version 1.1 a und 2,0 können Sie SNMP-basierte Netzwerk Verwaltungs Anwendungen entwickeln, die in der Windows-Umgebung ausgeführt werden.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039325"
---
# <a name="winsnmp-api"></a><span data-ttu-id="61088-104">WinSNMP-API</span><span class="sxs-lookup"><span data-stu-id="61088-104">WinSNMP API</span></span>

<span data-ttu-id="61088-105">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="61088-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61088-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="61088-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="61088-107">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="61088-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="61088-108">Mit der Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (der WinSNMP-API) Version 1.1 a und 2,0 können Sie SNMP-basierte Netzwerk Verwaltungs Anwendungen entwickeln, die in der Windows-Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="61088-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="61088-109">Das Simple Network Management-Protokoll (SNMP) ist ein Anforderungs Antwort Protokoll, das Verwaltungsinformationen zwischen Protokoll Entitäten überträgt.</span><span class="sxs-lookup"><span data-stu-id="61088-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="61088-110">WinSNMP wurde gemeinsam mit der Zusammenarbeit, der Eingabe und der Unterstützung von mehreren Unternehmen, Zuordnungen und Einzelpersonen entwickelt.</span><span class="sxs-lookup"><span data-stu-id="61088-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="61088-111">Der erste Teil dieser Übersicht enthält Informationen über den WinSNMP 2,0-Nachtrag, SNMP-Versionen und eine Liste der relevanten Anfragen für Kommentare (RFCs).</span><span class="sxs-lookup"><span data-stu-id="61088-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="61088-112">Außerdem werden das WinSNMP-Modell und die Komponenten und Funktionen der Microsoft WinSNMP-Implementierung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="61088-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="61088-113">Außerdem finden Sie hier Informationen zu Daten Verwaltungs-und Kommunikationskonzepten, die Sie in der WinSNMP-Umgebung programmieren müssen.</span><span class="sxs-lookup"><span data-stu-id="61088-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="61088-114">Im zweiten Abschnitt werden die WinSNMP-Funktionen und die folgenden verwandten WinSNMP-Programmieraufgaben erläutert:</span><span class="sxs-lookup"><span data-stu-id="61088-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="61088-115">Öffnen und Schließen einer WinSNMP-Anwendung</span><span class="sxs-lookup"><span data-stu-id="61088-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="61088-116">Öffnen und Schließen einer WinSNMP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="61088-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="61088-117">Verwalten von Traps und Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="61088-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="61088-118">Arbeiten mit Variablen Bindungs Listen</span><span class="sxs-lookup"><span data-stu-id="61088-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="61088-119">Arbeiten mit Protokolldaten Einheiten</span><span class="sxs-lookup"><span data-stu-id="61088-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="61088-120">Senden von SNMP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="61088-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="61088-121">Empfangen von SNMP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="61088-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="61088-122">Verwalten von Objekt bezeichlern</span><span class="sxs-lookup"><span data-stu-id="61088-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="61088-123">Freigeben von WinSNMP-Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="61088-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="61088-124">Festlegen des Entitäts-und Kontext Übersetzungsmodus</span><span class="sxs-lookup"><span data-stu-id="61088-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="61088-125">Verwalten der Richtlinie für Neuübertragungen</span><span class="sxs-lookup"><span data-stu-id="61088-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="61088-126">Schreiben von WinSNMP-Anwendungen mit mehreren Threads</span><span class="sxs-lookup"><span data-stu-id="61088-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="61088-127">Registrieren einer SNMP-Agent-Anwendung</span><span class="sxs-lookup"><span data-stu-id="61088-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="61088-128">Bevor Sie diese Übersicht lesen, sollten Sie mit den grundlegenden Konzepten der SNMP-und Windows-Programmierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="61088-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="61088-129">Weitere Informationen zu SNMP finden Sie unter [Simple Network Management Protocol (Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) ) und in den von der Internet Engineering Task Force (IETF) veröffentlichten Anforderungen für Kommentare (RFCs).</span><span class="sxs-lookup"><span data-stu-id="61088-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 