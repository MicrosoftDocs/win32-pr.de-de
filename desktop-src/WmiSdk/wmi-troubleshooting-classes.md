---
description: WMI stellt eine Reihe von Problem Behandlungs Klassen bereit, die von Skripts und Anwendungen verwendet werden können, um Informationen über den internen WMI-Status während der WMI-Kern-und Anbieter Vorgänge
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: WMI-Fehler Behebungs Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960795"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="8a639-103">WMI-Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="8a639-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="8a639-104">WMI stellt eine Reihe von Problem Behandlungs Klassen bereit, die von Skripts und Anwendungen verwendet werden können, um Informationen über den internen WMI-Status während der WMI-Kern-und Anbieter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="8a639-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="8a639-105">Weitere Informationen zur Problembehandlung für WMI finden Sie unter [WMI-Problem](wmi-troubleshooting.md) Behandlung und [Anbieter Konfiguration und Fehler Behebungs Klassen](provider-configuration-and-troubleshooting-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8a639-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="8a639-106">WMI verfügt über mehrere grundlegende Problem Behandlungs Klassen für WMI-Kern-und-Anbieter Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="8a639-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="8a639-107">**MSFT \_ WMIProvider-Leistungsindikatoren \_**</span><span class="sxs-lookup"><span data-stu-id="8a639-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="8a639-108">Auf jedem Computersystem wird nur eine dieser Klassen gefunden.</span><span class="sxs-lookup"><span data-stu-id="8a639-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="8a639-109">Es bietet eine Anzahl von verschiedenen Anbieter Vorgängen in diesem System.</span><span class="sxs-lookup"><span data-stu-id="8a639-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="8a639-110">**MSFT \_ wmiselfevent**</span><span class="sxs-lookup"><span data-stu-id="8a639-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="8a639-111">Die Ereignis Fehler Behebungs Klassen werden von [**MSFT \_ wmiselfevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8a639-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="8a639-112">Abfragen dieser Klasse geben Instanzen von Ereignis Klassen zurück, z. b. [**MSFT \_ wmithread poolcreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) oder [**MSFT \_ WMIProvider \_ kreateinstanceenumasyncevent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span><span class="sxs-lookup"><span data-stu-id="8a639-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="8a639-113">In der folgenden Liste finden Sie Links zu verschiedenen Kategorien von Ereignis Klassen, die von [**MSFT \_ wmiselfevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)abgeleitet werden:</span><span class="sxs-lookup"><span data-stu-id="8a639-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="8a639-114">Klassen zur Problembehandlung bei Anbieter Ereignissen</span><span class="sxs-lookup"><span data-stu-id="8a639-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="8a639-115">Consumerprovider-Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="8a639-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="8a639-116">Fehler Behebungs Klassen für WMI-Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8a639-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="8a639-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a639-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a639-118">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="8a639-118">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="8a639-119">Empfangen eines WMI-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="8a639-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
