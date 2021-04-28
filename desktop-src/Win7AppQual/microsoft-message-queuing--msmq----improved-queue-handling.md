---
description: 'Microsoft Message Queuing (MSMQ): Verbesserte Warteschlangenbehandlung'
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: 'Microsoft Message Queuing (MSMQ): Verbesserte Warteschlangenbehandlung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7b7b00cfce68a183d7925f7cfab5ff7ab54b9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088158"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="a316c-103">Microsoft Message Queuing (MSMQ): Verbesserte Warteschlangenbehandlung</span><span class="sxs-lookup"><span data-stu-id="a316c-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="a316c-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="a316c-104">Platforms</span></span>

<span data-ttu-id="a316c-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="a316c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="a316c-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a316c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="a316c-107">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="a316c-107">Feature Impact</span></span>

 <span data-ttu-id="a316c-108">**Schweregrad –** Niedrig</span><span class="sxs-lookup"><span data-stu-id="a316c-108">**Severity** - Low</span></span>  
<span data-ttu-id="a316c-109">**Häufigkeit** : Niedrig</span><span class="sxs-lookup"><span data-stu-id="a316c-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="a316c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a316c-110">Description</span></span>

<span data-ttu-id="a316c-111">Der MSMQ-Dienst legt keine harte Grenze für die Anzahl der Warteschlangen fest, die auf einem System erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="a316c-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="a316c-112">Die Leistung des Systems wird jedoch beeinträchtigt, wenn eine große Anzahl von Warteschlangen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a316c-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="a316c-113">Insbesondere wenn mehr als ein paar Tausend Warteschlangen vorhanden sind, erhöht sich die Startzeit des MSMQ-Diensts exponentiell, was zu sichtbaren Auswirkungen führt.</span><span class="sxs-lookup"><span data-stu-id="a316c-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="a316c-114">Microsoft hat das Starten des MSMQ-Diensts in Windows 7 optimiert, um den Suchaufwand für das Laden der Warteschlangen in den Arbeitsspeicher zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a316c-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="a316c-115">Diese Optimierung hat zu einer erheblichen Verbesserung der Startzeit des MSMQ-Diensts geführt, auch wenn mehrere Tausend Warteschlangen im System erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a316c-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="a316c-116">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="a316c-116">Manifestation of Impact</span></span>

<span data-ttu-id="a316c-117">Diese Leistungsverbesserung wirkt sich nicht auf die Funktionalität einer vorhandenen Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="a316c-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="a316c-118">Nutzen der geänderten Funktion</span><span class="sxs-lookup"><span data-stu-id="a316c-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="a316c-119">Anwendungsentwickler, die MSMQ unter Windows 7 verwenden, können jetzt ihre Lösungen entwerfen, ohne die Anzahl der Warteschlangen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="a316c-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="a316c-120">Beachten Sie, dass sich die Anzahl der Warteschlangen weiterhin auf die Gesamtleistung des MSMQ-Servers auswirkt, die Auswirkungen auf die Leistung jedoch jetzt linear und nicht exponentiell sind.</span><span class="sxs-lookup"><span data-stu-id="a316c-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="a316c-121">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests</span><span class="sxs-lookup"><span data-stu-id="a316c-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="a316c-122">Wenn Sie eine große Anzahl von Warteschlangen verwenden, simulieren Sie die Produktionsumgebung auf einem Testbett, überwachen Sie die Leistung, und analysieren Sie die Startzeit des Diensts und den Nachrichtendurchsatz mit einer großen Anzahl von Warteschlangen und Nachrichten, die im Testsystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a316c-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



