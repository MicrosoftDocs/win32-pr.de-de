---
title: Arbeiten mit Protokolldaten Einheiten
description: Das Simple Network Management-Protokoll (SNMP) sendet Vorgangs Anforderungen und-Antworten als SNMP-Nachrichten.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Arbeiten mit Protokolldaten Einheiten SNMP
- Protokolldaten Einheiten SNMP, arbeiten mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037281"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="f99d5-105">Arbeiten mit Protokolldaten Einheiten</span><span class="sxs-lookup"><span data-stu-id="f99d5-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="f99d5-106">Das Simple Network Management-Protokoll (SNMP) sendet Vorgangs Anforderungen und-Antworten als SNMP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f99d5-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="f99d5-107">Eine SNMP-Nachricht ist eine SNMP-Protokolldaten Einheit (PDU) und zusätzliche Nachrichten Header Elemente, die durch die relevante RFC definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f99d5-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="f99d5-108">Ein PDU enthält eine Variablen Bindungs Liste.</span><span class="sxs-lookup"><span data-stu-id="f99d5-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="f99d5-109">Die Struktur eines PDU ist auf die Microsoft WinSNMP-Implementierung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f99d5-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="f99d5-110">Eine WinSNMP-Anwendung kann mit einem Handle des Typs **hsnmp \_ PDU** auf ein PDU zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f99d5-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="f99d5-111">Die WinSNMP-Anwendung muss ein PDU erstellen, bevor Sie die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) oder die Funktion [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufruft.</span><span class="sxs-lookup"><span data-stu-id="f99d5-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="f99d5-112">Die Anwendung kann die Datenelemente eines PDU extrahieren und aktualisieren und die für PDUs zugewiesenen Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="f99d5-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="f99d5-113">Um diese Vorgänge auszuführen, verwendet die Anwendung die-Funktionen von WinSNMP [PDU](winsnmp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f99d5-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="f99d5-114">In der folgenden Tabelle sind Themen aufgeführt, in denen die Arbeit mit PDUs in der WinSNMP-Programmierumgebung erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="f99d5-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="f99d5-115">Thema</span><span class="sxs-lookup"><span data-stu-id="f99d5-115">Topic</span></span>                                                                        | <span data-ttu-id="f99d5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f99d5-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="f99d5-117">Erstellen eines PDU</span><span class="sxs-lookup"><span data-stu-id="f99d5-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="f99d5-118">Hier wird beschrieben, wie ein PDU erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f99d5-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="f99d5-119">Aktualisieren eines PDU</span><span class="sxs-lookup"><span data-stu-id="f99d5-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="f99d5-120">Hier wird beschrieben, wie PDU-Felder abgerufen und aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f99d5-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="f99d5-121">Duplizieren eines PDU</span><span class="sxs-lookup"><span data-stu-id="f99d5-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="f99d5-122">Beschreibt, wie ein PDU dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="f99d5-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="f99d5-123">Validieren eines PDU</span><span class="sxs-lookup"><span data-stu-id="f99d5-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="f99d5-124">Beschreibt die Validierung eines PDU.</span><span class="sxs-lookup"><span data-stu-id="f99d5-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="f99d5-125">Übereinstimmende Antworten und Anforderungs-PDUs</span><span class="sxs-lookup"><span data-stu-id="f99d5-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="f99d5-126">Beschreibt den Prozess der Übereinstimmung eines Antwort-PDU an eine Anforderungs-PDU.</span><span class="sxs-lookup"><span data-stu-id="f99d5-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="f99d5-127">Weitere Informationen finden Sie unter [Arbeiten mit Variablen Bindungs Listen](working-with-variable-binding-lists.md) und [Ressourcen handle-Objekten](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f99d5-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 




