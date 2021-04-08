---
title: Informationen zu Bluetooth
description: Bluetooth ist ein Industriestandard Protokoll, das drahtlose Konnektivität für eine Vielzahl von Geräten ermöglicht, einschließlich Computern, Druckern, Mobiltelefonen und Hand Held Geräten.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, beschrieben
- Bluetooth Bluetooth, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038603"
---
# <a name="about-bluetooth"></a><span data-ttu-id="3b70a-105">Informationen zu Bluetooth</span><span class="sxs-lookup"><span data-stu-id="3b70a-105">About Bluetooth</span></span>

<span data-ttu-id="3b70a-106">Bluetooth ist ein Industriestandard Protokoll, das drahtlose Konnektivität für eine Vielzahl von Geräten ermöglicht, einschließlich Computern, Druckern, Mobiltelefonen und Hand Held Geräten.</span><span class="sxs-lookup"><span data-stu-id="3b70a-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="3b70a-107">Zu den wichtigsten Bluetooth-Features gehören:</span><span class="sxs-lookup"><span data-stu-id="3b70a-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="3b70a-108">Kostengünstiger drahtlos Protokoll mit geringem Energieverbrauch mit Industriestandard-Unterstützung und weltweiten Akzeptanz.</span><span class="sxs-lookup"><span data-stu-id="3b70a-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="3b70a-109">Eine definierte und vertraute Programmierschnittstelle, mit der Entwickler Anwendungen schnell entwickeln oder portieren können.</span><span class="sxs-lookup"><span data-stu-id="3b70a-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="3b70a-110">Eine offizielle Website und eine branchenweite kooperative Organisation, in der Bluetooth-Technologie erläutert, herauf gestuft und standardisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b70a-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="3b70a-111">Weitere Informationen finden Sie unter [www.Bluetooth.com](https://www.bluetooth.com/).</span><span class="sxs-lookup"><span data-stu-id="3b70a-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="3b70a-112">Bluetooth unter Windows bietet Kerndienste, die mit den von Transmission Control Protocol (TCP/IP) verfügbar gemachten Diensten vergleichbar sind.</span><span class="sxs-lookup"><span data-stu-id="3b70a-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="3b70a-113">Wie viele Netzwerkprotokolle und-Dienste werden Bluetooth-Konnektivität und Datenübertragung mithilfe von Windows Sockets-Funktionsaufrufen programmiert, wobei gängige Windows Sockets-Programmiertechniken und bestimmte Bluetooth-Erweiterungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b70a-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="3b70a-114">Da jedoch bedeutende Unterschiede zwischen einem verkabelten, einem Netzwerk und einem drahtlosen Ad-hoc-Netzwerk bestehen, bietet Bluetooth Erweiterungen wie die Dienst-/gerätermittlung und die Benachrichtigung, mit deren Hilfe Anwendungen in der drahtlos Umgebung ordnungsgemäß ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3b70a-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="3b70a-115">Diese Erweiterungen haben auch die Möglichkeit, eine einfache Portierung auf ähnliche Technologien wie z. b. UNDA oder zukünftige drahtlose Transporte zu portieren.</span><span class="sxs-lookup"><span data-stu-id="3b70a-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="3b70a-116">Microsoft bietet Unterstützung für Bluetooth unter Windows XP mit Service Pack 1 (SP1) und höher, unter Windows XP Embedded mit Service Pack 2 und auf Windows CE.</span><span class="sxs-lookup"><span data-stu-id="3b70a-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="3b70a-117">Bluetooth-Anwendungen, die unter Windows XP ausgeführt werden, sollten in einem Windows XP Embedded-basierten Lauf Zeit Abbild ausgeführt werden können, das die erforderlichen Abhängigkeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="3b70a-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="3b70a-118">Weitere Informationen zu Windows XP Embedded finden Sie in der Hilfe Dokumentation zu Windows XP Embedded auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="3b70a-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="3b70a-119">Weitere Informationen zur Windows CE Programmierung finden Sie im Windows CE SDK.</span><span class="sxs-lookup"><span data-stu-id="3b70a-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="3b70a-120">Microsoft bietet zwei Ansätze zum Programmieren von Bluetooth unter Windows:</span><span class="sxs-lookup"><span data-stu-id="3b70a-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="3b70a-121">Verwenden der Windows Sockets-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b70a-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="3b70a-122">Direktes Verwalten von Geräten mithilfe von nicht-Socket-Bluetooth-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3b70a-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="3b70a-123">In diesem Abschnitt finden Sie eine Übersicht über diese beiden Ansätze in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="3b70a-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="3b70a-124">Weitere Informationen zum Verwenden der Windows Sockets-API-Elemente zum Programmieren von Bluetooth finden Sie unter [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="3b70a-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="3b70a-125">`Section`</span><span class="sxs-lookup"><span data-stu-id="3b70a-125">Section</span></span>                                                                                | <span data-ttu-id="3b70a-126">Inhalt</span><span class="sxs-lookup"><span data-stu-id="3b70a-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="3b70a-127">Windows Sockets-Unterstützung für Bluetooth</span><span class="sxs-lookup"><span data-stu-id="3b70a-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="3b70a-128">Beschreibt die Beziehung zwischen Bluetooth und Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="3b70a-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="3b70a-129">Verwalten von Bluetooth-Geräten und-Diensten</span><span class="sxs-lookup"><span data-stu-id="3b70a-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="3b70a-130">Hier wird beschrieben, wie Bluetooth-Geräte und-Dienste verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3b70a-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




