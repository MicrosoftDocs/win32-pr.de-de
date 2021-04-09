---
description: Es gibt fünf Arten von Ereignissen, die protokolliert werden können. Alle diese verfügen über klar definierte allgemeine Daten und können optional ereignisspezifische Daten einschließen.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Ereignistypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864244"
---
# <a name="event-types"></a><span data-ttu-id="84887-104">Ereignistypen</span><span class="sxs-lookup"><span data-stu-id="84887-104">Event Types</span></span>

<span data-ttu-id="84887-105">Es gibt fünf Arten von Ereignissen, die protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="84887-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="84887-106">Alle diese verfügen über klar definierte allgemeine Daten und können optional ereignisspezifische Daten einschließen.</span><span class="sxs-lookup"><span data-stu-id="84887-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="84887-107">Die Anwendung gibt den Ereignistyp an, wenn ein Ereignis gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="84887-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="84887-108">Jedes Ereignis muss einen einzelnen Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="84887-108">Each event must be of a single type.</span></span> <span data-ttu-id="84887-109">Die Ereignisanzeige zeigt ein anderes Symbol für jeden Typ in der Listenansicht des Ereignis Protokolls an.</span><span class="sxs-lookup"><span data-stu-id="84887-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="84887-110">In der folgenden Tabelle werden die fünf bei der Ereignisprotokollierung verwendeten Ereignis Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84887-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="84887-111">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="84887-111">Event type</span></span>        | <span data-ttu-id="84887-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84887-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84887-113">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="84887-113">**Error**</span></span>         | <span data-ttu-id="84887-114">Ein Ereignis, das auf ein erhebliches Problem hinweist, z. b. Datenverlust oder Funktionsverlust.</span><span class="sxs-lookup"><span data-stu-id="84887-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="84887-115">Wenn beispielsweise ein Dienst beim Starten nicht geladen werden kann, wird ein Fehler Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="84887-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="84887-116">**Warnung**</span><span class="sxs-lookup"><span data-stu-id="84887-116">**Warning**</span></span>       | <span data-ttu-id="84887-117">Ein Ereignis, das nicht unbedingt wichtig ist, aber möglicherweise auf ein mögliches zukünftiges Problem hinweist.</span><span class="sxs-lookup"><span data-stu-id="84887-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="84887-118">Wenn z. b. Speicherplatz auf dem Datenträger niedrig ist, wird ein Warn Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="84887-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="84887-119">Wenn eine Anwendung nach einem Ereignis ohne Verlust von Funktionen oder Daten wieder hergestellt werden kann, kann Sie das Ereignis in der Regel als Warn Ereignis klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="84887-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="84887-120">**Information**</span><span class="sxs-lookup"><span data-stu-id="84887-120">**Information**</span></span>   | <span data-ttu-id="84887-121">Ein Ereignis, das den erfolgreichen Betrieb einer Anwendung, eines Treibers oder eines Dienstanbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="84887-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="84887-122">Wenn ein Netzwerktreiber z. b. erfolgreich geladen wird, kann es sinnvoll sein, ein Informations Ereignis zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="84887-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="84887-123">Beachten Sie, dass es für eine Desktop Anwendung grundsätzlich ungeeignet ist, bei jedem Start ein Ereignis zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="84887-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="84887-124">**Erfolgsüberwachung**</span><span class="sxs-lookup"><span data-stu-id="84887-124">**Success Audit**</span></span> | <span data-ttu-id="84887-125">Ein Ereignis, das einen erfolgreichen überwachten Sicherheits Zugriffs Versuch aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="84887-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="84887-126">Beispielsweise wird der Versuch eines Benutzers, sich am System anzumelden, als Erfolgs Überwachungs Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="84887-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="84887-127">**Fehlerüberwachung**</span><span class="sxs-lookup"><span data-stu-id="84887-127">**Failure Audit**</span></span> | <span data-ttu-id="84887-128">Ein Ereignis, das einen überwachten Sicherheits Zugriffs Versuch aufzeichnet, der fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="84887-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="84887-129">Wenn ein Benutzer beispielsweise versucht, auf ein Netzwerklaufwerk zuzugreifen und einen Fehler verursacht, wird der Versuch als Fehler Überwachungs Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="84887-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="84887-130">Die ausgewählten Aktivitäten von Benutzern können durch die Überwachung von Sicherheits Ereignissen und das anschließende Platzieren von Einträgen im Sicherheitsprotokoll eines Computers verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="84887-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 



