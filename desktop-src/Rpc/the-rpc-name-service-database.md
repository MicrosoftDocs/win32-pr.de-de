---
title: Datenbank des RPC-namens Dienstanbieter
description: Ein Namensdienst ist ein Dienst, der-Objekten Namen zuordnet und in der Regel die (Name, Object)-Paare in einer Datenbank verwaltet.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Name Service Database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471421"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="4bfe7-104">Datenbank des RPC-namens Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4bfe7-104">The RPC Name Service Database</span></span>

<span data-ttu-id="4bfe7-105">Ein Namensdienst ist ein Dienst, der-Objekten Namen zuordnet und in der Regel die (Name, Object)-Paare in einer Datenbank verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="4bfe7-106">Im Allgemeinen ist der Name ein logischer Name, den Benutzer leicht merken und verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="4bfe7-107">Beispielsweise kann ein Benutzer mit einem Namensdienst den logischen Namen "Laser Printer" verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="4bfe7-108">Der Namensdienst ordnet diesen Namen dem vom Druckserver verwendeten Netzwerk spezifischen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="4bfe7-109">Um eine vereinfachte Erläuterung zu verwenden, ordnet der RPC-Namensdienst einem Bindungs handle einen Namen zu und verwaltet die Zuordnungen (Name, Bindungs handle) in der Datenbank des RPC-namens Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="4bfe7-110">Der RPC-Namensdienst ermöglicht es Client Anwendungen, anstelle einer bestimmten Protokoll Sequenz und Netzwerkadresse einen logischen Namen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="4bfe7-111">Die Verwendung des logischen Namens erleichtert Netzwerkadministratoren die Installation und Konfiguration der verteilten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="4bfe7-112">Ein RPC Name Service-Datenbankeintrag weist eines der folgenden Attribute auf: **Server**, **Gruppe** oder **Profil**.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="4bfe7-113">In der Microsoft-Implementierung können Einträge nur ein Attribut aufweisen, sodass diese Einträge auch als Server Einträge, Gruppen Einträge und Profil Einträge bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="4bfe7-114">Der Server Eintrag besteht aus den Schnittstellen-UUIDs, den Objekt-UUIDs (erforderlich, wenn der Server mehrere Einstiegspunkte implementiert), der Netzwerkadresse, der Protokoll Sequenz und sämtlicher Endpunkt Informationen, die bekannten Endpunkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="4bfe7-115">Wenn ein dynamischer Endpunkt verwendet wird, werden die Endpunkt Informationen in der Datenbank der Endpunkt Zuordnung und nicht in der Name Service-Datenbank gespeichert, und der Endpunkt wird wie jeder andere dynamische Endpunkt aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="4bfe7-116">Server Einträge werden von Funktionen verwaltet, die mit dem Präfix "rpcnsbinding" beginnen.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="4bfe7-117">Der Gruppen Eintrag kann Server Einträge oder andere Gruppen Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="4bfe7-118">Gruppen Einträge werden von Funktionen verwaltet, die mit dem Präfix "rpcnsgroup" beginnen.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="4bfe7-119">Der Profil Eintrag kann Profil-, Gruppen-oder Server Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="4bfe7-120">Profil Einträge werden von den Funktionen verwaltet, die mit dem Präfix "rpcnsprofile" beginnen.</span><span class="sxs-lookup"><span data-stu-id="4bfe7-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="4bfe7-121">Dieser Abschnitt enthält eine Übersicht über die Name Service-Datenbank in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4bfe7-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="4bfe7-122">Richtlinien für die Namensdienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="4bfe7-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="4bfe7-123">Übersicht über den Eintrag "Name Service"</span><span class="sxs-lookup"><span data-stu-id="4bfe7-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="4bfe7-124">Kriterien für Namensdienst Einträge</span><span class="sxs-lookup"><span data-stu-id="4bfe7-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="4bfe7-125">Bereinigung der Namensdienst Einträge</span><span class="sxs-lookup"><span data-stu-id="4bfe7-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="4bfe7-126">Was geschieht während einer Abfrage?</span><span class="sxs-lookup"><span data-stu-id="4bfe7-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="4bfe7-127">Verwenden von Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="4bfe7-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="4bfe7-128">Verwenden des Zellen Verzeichnis Dienstanbieter (CDs)</span><span class="sxs-lookup"><span data-stu-id="4bfe7-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="4bfe7-129">Namens Syntax</span><span class="sxs-lookup"><span data-stu-id="4bfe7-129">Name Syntax</span></span>](name-syntax.md)

 

 




