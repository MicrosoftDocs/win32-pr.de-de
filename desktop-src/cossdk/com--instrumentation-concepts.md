---
description: Der com+-Instrumentations Dienst ermöglicht es Ihnen, ihre eigenen com+-ereignisverwaltungs-und Protokollierungs Programme zu erstellen, wenn Sie verschiedene Leistungsmetriken für Ihre COM+-Komponenten anzeigen möchten.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Com+-Instrumentations Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346849"
---
# <a name="com-instrumentation-concepts"></a><span data-ttu-id="52b70-103">Com+-Instrumentations Konzepte</span><span class="sxs-lookup"><span data-stu-id="52b70-103">COM+ Instrumentation Concepts</span></span>

<span data-ttu-id="52b70-104">Der com+-Instrumentations Dienst ermöglicht es Ihnen, ihre eigenen com+-ereignisverwaltungs-und Protokollierungs Programme zu erstellen, wenn Sie verschiedene Leistungsmetriken für Ihre COM+-Komponenten anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="52b70-104">The COM+ instrumentation service enables you to build your own COM+ event management and logging programs when you want to display various performance metrics for your COM+ components.</span></span> <span data-ttu-id="52b70-105">Die com+-Instrumentation kann auch verwendet werden, um benutzerdefinierte Ereignisse zu konfigurieren und com+-Ereignisse in Visual Studio Analyzer Format (VSA) zu konvertieren, wenn Sie die MTS-Pakete aktualisieren, die MTS-Ereignisse empfangen.</span><span class="sxs-lookup"><span data-stu-id="52b70-105">COM+ instrumentation can also be used to configure user-defined events and to convert COM+ events to Visual Studio Analyzer (VSA) format when you are upgrading MTS packages that are receiving MTS events.</span></span>

> [!Note]  
> <span data-ttu-id="52b70-106">Ab Windows Server 2003 verfügen nur Administratoren über Lese Zugriffsberechtigungen für die Ablauf Verfolgungs Protokolle für Systemereignisse.</span><span class="sxs-lookup"><span data-stu-id="52b70-106">As of Windows Server 2003, only administrators have read access privileges to the trace logs for system events.</span></span>

 

<span data-ttu-id="52b70-107">Durch Abonnieren der vom System Events Publisher veröffentlichten Ereignisse können Clients die [com+-Instrumentierungs Schnittstellen](com--instrumentation-interfaces.md) implementieren, um Benachrichtigungen für eine Reihe von com+-Leistungsmetriken zu erhalten, z. b. Informationen zu bestimmten COM+-Objekten, com+-Anwendungen und com+-Diensten.</span><span class="sxs-lookup"><span data-stu-id="52b70-107">By subscribing to the events published by the system events publisher, clients can implement the [COM+ instrumentation interfaces](com--instrumentation-interfaces.md) to receive notifications for a variety of COM+ performance metrics, such as information about specific COM+ objects, COM+ applications, and COM+ services.</span></span> <span data-ttu-id="52b70-108">Die Metriken werden auf dem Client mit dem [com+](com--events.md)-Ereignis Dienst veröffentlicht, einem LCE-System (lose gekoppelte Ereignisse), das Ereignis Informationen von verschiedenen Verlegern in einem Ereignisspeicher im com+-Katalog speichert.</span><span class="sxs-lookup"><span data-stu-id="52b70-108">The metrics are published to the client by using the [COM+ events service](com--events.md), a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.</span></span>

> [!Note]  
> <span data-ttu-id="52b70-109">Die com+-Instrumentation garantiert nicht die Übermittlung eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="52b70-109">COM+ instrumentation does not guarantee the delivery of an event.</span></span>

 

<span data-ttu-id="52b70-110">Jede Metrik verfügt über einen Zeitstempel, der die Uhrzeit angibt, zu der die Metrik generiert wurde, und nicht die Uhrzeit, zu der Sie gesendet oder empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="52b70-110">Every metric has a timestamp that indicates the time when the metric was generated, not the time that it was dispatched or received.</span></span> <span data-ttu-id="52b70-111">Der Client kann den Zeitstempel korrelieren und die Kosten für die Ausführung einer COM+-Anwendung, die Kosten einer Transaktion, die in einer COM+-Anwendung ausgeführt wird, oder die Kosten eines Methoden Aufrufes in einer COM+-Anwendung ermitteln.</span><span class="sxs-lookup"><span data-stu-id="52b70-111">The client can correlate the timestamp and find out the cost of running a COM+ application, the cost of a transaction executed inside a COM+ application, or the cost of a method call inside of a COM+ application.</span></span>

<span data-ttu-id="52b70-112">Sie können den com+-Instrumentations Dienst auch verwenden, um nach den spezifischen leistungsmetrikinformationen zu filtern, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="52b70-112">You can also use the COM+ Instrumentation service to filter for the specific performance metrics information that you want to see.</span></span> <span data-ttu-id="52b70-113">Wenn Sie z. b. eine com+-Instrumentations Schnittstelle oder-Methode abonnieren, können Sie die Eigenschaften für das Abonnement in der [**comsvcereiginfo**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) -Struktur angeben, z. b. die Anwendungs-ID (**guidapp** -Member) oder die Prozess-ID (**dwpid** -Member).</span><span class="sxs-lookup"><span data-stu-id="52b70-113">For example, when you subscribe to a COM+ instrumentation interface or method, you can specify properties for the subscription in the [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) structure, such as the application ID (**guidApp** member) or the process ID (**dwPid** member).</span></span>

<span data-ttu-id="52b70-114">Wenn die Anwendungs-ID angegeben ist, erhalten Sie nur die Metriken aus der angegebenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="52b70-114">When the application ID is specified, you receive only the metrics from the specified application.</span></span> <span data-ttu-id="52b70-115">Wenn die Prozess-ID angegeben ist, erhalten Sie Metriken von der angegebenen Serveranwendung und den Bibliotheksanwendungen, die in diesem Prozess geladen werden.</span><span class="sxs-lookup"><span data-stu-id="52b70-115">When the process ID is specified, you receive metrics from the specified server application and library applications that are loaded in that process.</span></span> <span data-ttu-id="52b70-116">Der Benutzer kann sowohl die Anwendungs-ID als auch die Prozess-ID angeben, aber die Anwendungs-ID muss die der Serveranwendung sein, die im Prozess mit der angegebenen Prozess-ID ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52b70-116">The user can specify both the application ID and the process ID, but the application ID has to be that of the server application running in the process with the specified process ID.</span></span> <span data-ttu-id="52b70-117">Wenn keines von beiden angegeben ist, empfängt der Benutzer Metriken von allen Server-und Bibliotheksanwendungen.</span><span class="sxs-lookup"><span data-stu-id="52b70-117">If neither is specified, the user receives metrics from all the server and library applications.</span></span>

<span data-ttu-id="52b70-118">Die com+-Instrumentierungs Metriken bieten genügend Informationen, damit die Überwachungsanwendung Sie mit den betriebssystemmetriken für Leistungsanalysen, Kapazitätsplanung und Modellierung und Vorhersage korrelieren kann.</span><span class="sxs-lookup"><span data-stu-id="52b70-118">The COM+ instrumentation metrics provide enough information for the monitoring application to correlate them with the operating system metrics for performance analysis, capacity planning, and for modeling and prediction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52b70-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52b70-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52b70-120">Com+-Instrumentierungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="52b70-120">COM+ Instrumentation Interfaces</span></span>](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



