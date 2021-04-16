---
description: Die folgende Abbildung zeigt die Beziehung zwischen Monitoren und anderen Komponenten der Netzwerkmonitor Architektur.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Monitor Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551686"
---
# <a name="monitor-architecture"></a><span data-ttu-id="3f366-103">Monitor Architektur</span><span class="sxs-lookup"><span data-stu-id="3f366-103">Monitor Architecture</span></span>

<span data-ttu-id="3f366-104">Die folgende Abbildung zeigt die Beziehung zwischen [*Monitoren*](m.md) und anderen Komponenten der Netzwerkmonitor Architektur.</span><span class="sxs-lookup"><span data-stu-id="3f366-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![Beziehung zwischen Monitoren und anderen Komponenten des Netzwerk Monitors](images/nmarch2.png)

<span data-ttu-id="3f366-106">Der Netzwerk Datenverkehr wird (als einzelne Frames) vom NDIS-Treiber gesammelt.</span><span class="sxs-lookup"><span data-stu-id="3f366-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="3f366-107">Der Netzwerkmonitor Treiber (Nmnt.sys) leitet die Frames dann an einen Netzwerk Paketanbieter (NPP) weiter, der wiederum die Daten im Echtzeitmodus erfasst.</span><span class="sxs-lookup"><span data-stu-id="3f366-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="3f366-108">Der npp ist eine Sammlung von COM-Schnittstellen, die zum Erfassen von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f366-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="3f366-109">In diesem Fall wird die Schnittstelle " [**untc**](irtc.md) " verwendet, um eine echt Zeiterfassung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3f366-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="3f366-110">Der NPP wird für verzögerte und Echt Zeit Erfassungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f366-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="3f366-111">Bei verzögerten Erfassungen, die von Experten und Parser verwendet werden, wird die [**idelta-DC**](idelaydc.md) -Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f366-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="3f366-112">Der Monitor überprüft dann die erfassten Daten im Echtzeitmodus und erkennt bestimmte Netzwerkbedingungen und erzeugt Ereignisse nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="3f366-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="3f366-113">Drei weitere Komponenten werden von Überwachungsanwendungen verwendet: das Überwachungs Steuerungs Tool, der Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) und die Ereignisanzeige:</span><span class="sxs-lookup"><span data-stu-id="3f366-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="3f366-114">Das Monitor Steuerungs Tool wird zum Verwalten von Monitor Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f366-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="3f366-115">Dies umfasst das Konfigurieren und Ausführen aller ihrer Monitor Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3f366-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="3f366-116">Der Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) löst Ereignisse aus, stellt für die Ereignisanzeige einen Kommunikationslink zu WMI bereit und koordiniert die Verarbeitung von Monitor Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="3f366-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="3f366-117">Die Ereignisanzeige zeigt die vom Monitor Steuerungs Dienst ausgelösten Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="3f366-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f366-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f366-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f366-119">**Imonitor**</span><span class="sxs-lookup"><span data-stu-id="3f366-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="3f366-120">**Imonitoreventer Enter**</span><span class="sxs-lookup"><span data-stu-id="3f366-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="3f366-121">**"Iran"**</span><span class="sxs-lookup"><span data-stu-id="3f366-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



