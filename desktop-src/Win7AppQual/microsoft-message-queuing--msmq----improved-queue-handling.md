---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ)-verbesserte Warteschlangen Behandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959958"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="afd97-103">Microsoft Message Queuing (MSMQ)-verbesserte Warteschlangen Behandlung</span><span class="sxs-lookup"><span data-stu-id="afd97-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="afd97-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="afd97-104">Platforms</span></span>

<span data-ttu-id="afd97-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="afd97-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="afd97-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afd97-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="afd97-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="afd97-107">Feature Impact</span></span>

 <span data-ttu-id="afd97-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="afd97-108">**Severity** - Low</span></span>  
<span data-ttu-id="afd97-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="afd97-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="afd97-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afd97-110">Description</span></span>

<span data-ttu-id="afd97-111">Der MSMQ-Dienst schränkt die Anzahl der Warteschlangen, die auf einem System erstellt werden können, nicht ein.</span><span class="sxs-lookup"><span data-stu-id="afd97-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="afd97-112">Die Leistung des Systems ist jedoch beeinträchtigt, wenn eine große Anzahl von Warteschlangen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="afd97-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="afd97-113">Insbesondere bei mehr als wenigen tausend Warteschlangen erhöht sich die Startzeit des MSMQ-Dienstanbieter exponentiell, was zu einer sichtbaren Auswirkung führt.</span><span class="sxs-lookup"><span data-stu-id="afd97-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="afd97-114">Microsoft hat den MSMQ-Dienst Start in Windows 7 optimiert, um den Suchaufwand für das Laden der Warteschlangen in den Arbeitsspeicher zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="afd97-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="afd97-115">Diese Optimierung hat zu einer drastischen Verbesserung der Startzeit des MSMQ-Dienstanbieter geführt, auch wenn mehrere tausend Warteschlangen im System erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="afd97-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="afd97-116">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="afd97-116">Manifestation of Impact</span></span>

<span data-ttu-id="afd97-117">Diese Leistungsverbesserung wirkt sich nicht auf die Funktionalität einer vorhandenen Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="afd97-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="afd97-118">Nutzen der geänderten Funktion</span><span class="sxs-lookup"><span data-stu-id="afd97-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="afd97-119">Anwendungsentwickler, die MSMQ unter Windows 7 verwenden, können jetzt Ihre Lösungen entwerfen, ohne die Anzahl der Warteschlangen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="afd97-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="afd97-120">Beachten Sie, dass sich die Anzahl der Warteschlangen weiterhin auf die Gesamtleistung des MSMQ-Servers auswirkt, aber die Auswirkungen auf die Leistung auf eine lineare statt auf exponentielle Skalierung.</span><span class="sxs-lookup"><span data-stu-id="afd97-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="afd97-121">Kompatibilitäts-, Leistungs-, Zuverlässigkeits-und Nutz barkeits Tests</span><span class="sxs-lookup"><span data-stu-id="afd97-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="afd97-122">Wenn Sie eine große Anzahl von Warteschlangen verwenden, simulieren Sie die Produktionsumgebung auf einem Testkonto, überwachen Sie die Leistung, und analysieren Sie die Startzeit und den Nachrichten Durchsatz mit einer großen Anzahl von Warteschlangen und Nachrichten, die im Testsystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="afd97-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



