---
description: Netzwerk Paketanbieter (NPPs) stellen COM-Schnittstellen bereit, die von NPP-Anwendungen aufgerufen werden, und Netzwerkmonitor.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: NPP-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355518"
---
# <a name="npp-interfaces"></a><span data-ttu-id="577df-103">NPP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="577df-103">NPP Interfaces</span></span>

<span data-ttu-id="577df-104">Netzwerk Paketanbieter (NPPs) stellen COM-Schnittstellen bereit, die von NPP-Anwendungen aufgerufen werden, und Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="577df-104">Network packet providers (NPPs) provide COM interfaces that are called by NPP applications, and Network Monitor.</span></span> <span data-ttu-id="577df-105">Beachten Sie beim Aufrufen von " [comatenppinterface](createnppinterface.md)", dass jede NPP als einzelnes in-Process-COM-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="577df-105">When you call [CreateNPPInterface](createnppinterface.md), remember that each NPP is represented as a single in-process COM object.</span></span> <span data-ttu-id="577df-106">Anwendungen können eine beliebige Anzahl von NPP-Objekten instanziieren.</span><span class="sxs-lookup"><span data-stu-id="577df-106">Applications can instantiate any number of NPP objects.</span></span> <span data-ttu-id="577df-107">Allerdings muss jedes instanziierte Objekt nur eine – und nur eine – der fünf NPP-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="577df-107">However, each instantiated object must use one—and only one—of the five NPP interfaces.</span></span>

<span data-ttu-id="577df-108">Beachten Sie auch, dass unterschiedliche NPP-Schnittstellen Netzwerkdaten in verschiedenen Formularen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="577df-108">Note also that different NPP interfaces provide network data in various forms.</span></span> <span data-ttu-id="577df-109">Netzwerkmonitor z. b. die **idelta-DC** -Schnittstelle verwendet, um Netzwerk Datenverkehr zu erfassen und in einer Erfassungs Datei zu speichern. während Monitore den Netzwerk Datenverkehr in Echtzeit mithilfe der " **untc** "-Schnittstelle erfassen.</span><span class="sxs-lookup"><span data-stu-id="577df-109">For example, Network Monitor uses the **IDelaydC** interface to capture network traffic and save it to a capture file; while monitors use the **IRTC** interface to capture real time network traffic.</span></span> <span data-ttu-id="577df-110">In der folgenden Tabelle werden Netzwerkmonitor NPP-Schnittstellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="577df-110">The following table describes Network Monitor NPP interfaces.</span></span>



| <span data-ttu-id="577df-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="577df-111">Interface</span></span>                | <span data-ttu-id="577df-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="577df-112">Description</span></span>                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="577df-113">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="577df-113">IDelaydC</span></span>](idelaydc.md) | <span data-ttu-id="577df-114">Erfasst Netzwerk Datenverkehr, der in einer Erfassungs Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="577df-114">Captures network traffic that is stored in a capture file.</span></span> <span data-ttu-id="577df-115">Diese Schnittstelle wird von Netzwerkmonitor-und NPP-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="577df-115">This interface is used by Network Monitor and NPP applications.</span></span>                                          |
| [<span data-ttu-id="577df-116">IESP</span><span class="sxs-lookup"><span data-stu-id="577df-116">IESP</span></span>](iesp.md)         | <span data-ttu-id="577df-117">Erfasst Netzwerk Datenverkehr, der in einer Erfassungs Datei gespeichert ist, und stellt erweiterte Statistiken in einem speziellen ESP-Dateiformat bereit.</span><span class="sxs-lookup"><span data-stu-id="577df-117">Captures network traffic that is stored in a capture file and provides enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="577df-118">Diese Schnittstelle wird von NPP-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="577df-118">This interface is used by NPP applications</span></span> |
| [<span data-ttu-id="577df-119">"Iran"</span><span class="sxs-lookup"><span data-stu-id="577df-119">IRTC</span></span>](irtc.md)         | <span data-ttu-id="577df-120">Erfasst Netzwerk Datenverkehr in Echtzeit und löst Ereignisse aus, wenn diese auftreten.</span><span class="sxs-lookup"><span data-stu-id="577df-120">Captures real time network traffic and triggers events when they occur.</span></span> <span data-ttu-id="577df-121">Diese Schnittstelle wird von [*Monitoren*](m.md) und NPP-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="577df-121">This interface is used by [*monitors*](m.md) and NPP applications.</span></span>     |
| [<span data-ttu-id="577df-122">IStats</span><span class="sxs-lookup"><span data-stu-id="577df-122">IStats</span></span>](istats.md)     | <span data-ttu-id="577df-123">Ruft Statistiken als Rohdaten und nicht als Frames ab.</span><span class="sxs-lookup"><span data-stu-id="577df-123">Retrieves statistics as raw data rather than frames.</span></span> <span data-ttu-id="577df-124">Diese Schnittstelle wird von NPP-Anwendungen wie [*Perfmon*](p.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="577df-124">This interface is used by NPP applications such as [*Perfmon*](p.md).</span></span>                     |



 

 

 



