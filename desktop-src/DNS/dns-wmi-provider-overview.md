---
title: DNS WMI-Anbieter (Übersicht)
description: Ein Anbieter ist ein Architektur Element von Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, WMI-Anbieter, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036833"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="d1ed1-104">DNS WMI-Anbieter (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="d1ed1-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="d1ed1-105">Ein Anbieter ist ein Architektur Element von *Windows-Verwaltungsinstrumentation (WMI)*.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="d1ed1-106">WMI definiert eine einheitliche Architektur zum beschreiben, zugreifen auf und Instrumentieren von Objekten.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="d1ed1-107">Ein Teil dieser Architektur ist eine große Datenbank von WMI-Klassen, die zum Ausführen von Remote Verwaltungsaufgaben für bestimmte Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="d1ed1-108">WMI-Anbieter fungieren als Vermittler zwischen WMI und einem oder mehreren verwalteten Objekten.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="d1ed1-109">Wenn WMI eine Anforderung von einer Verwaltungs Anwendung für Daten empfängt, die nicht im CIM-Repository verfügbar sind, oder für Benachrichtigungen von Ereignissen, die von WMI nicht unterstützt werden, wird die Anforderung an einen Anbieter weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="d1ed1-110">Anbieter stellen Daten und Ereignisbenachrichtigungen für verwaltete Objekte bereit, die für die jeweilige Domäne spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="d1ed1-111">Ein Anbieter erweitert das WMI-Schema der Klassen, damit WMI mit neuen Objekttypen arbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="d1ed1-112">Der DNS-WMI-Anbieter definiert Klassen zum Abfragen und Konfigurieren eines DNS-Servers sowie die zugehörigen DNS-Zonen und DNS-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="d1ed1-113">Der DNS-WMI-Anbieter macht für Clients eine Reihe von DNS-Objekten verfügbar, einschließlich DNS-Server, DNS-Domäne und DNS-RR-Objekten.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="d1ed1-114">Über diese Objekte können Clients DNS-Verwaltungsaktivitäten durchführen.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="d1ed1-115">Mit dem DNS-WMI-Anbieter können Sie eigene Tools erstellen, um die meisten Verwaltungsaufgaben für DNS-Server auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="d1ed1-116">Beispielsweise können Sie Zonen und Datensätze erstellen, löschen und anzeigen. Server-und Zonen Eigenschaften zurücksetzen; und führen routinemäßige Verwaltungsvorgänge aus, z. b. das Aktualisieren der Zone, das erneute Laden der Zone, das Aktualisieren der Zone, das Zurückschreiben der Zone in eine Datei oder Active Directory, das Anhalten und Fortsetzen der Zone, das Löschen des Caches, das Beenden und Starten des DNS-Dienstes und das Anzeigen von Statistiken.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="d1ed1-117">Der DNS-WMI-Anbieter verfügt über eine Reihe eindeutiger Verhalten, die in anderen Anbietern nicht gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="d1ed1-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="d1ed1-118">Klassen Details finden Sie in der [DNS-WMI-Anbieter Referenz](dns-wmi-provider-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ed1-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 




