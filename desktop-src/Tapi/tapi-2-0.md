---
description: TAPI 2,0 bietet eine kleine Anzahl von Verbesserungen an der grundlegenden TAPI 1,4-Funktionalität.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345428"
---
# <a name="tapi-20"></a><span data-ttu-id="b2184-103">TAPI 2,0</span><span class="sxs-lookup"><span data-stu-id="b2184-103">TAPI 2.0</span></span>

<span data-ttu-id="b2184-104">TAPI 2,0 bietet eine kleine Anzahl von Verbesserungen an der grundlegenden TAPI 1,4-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="b2184-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="b2184-105">Es gab jedoch einige wesentliche Änderungen an der Architektur, die die Stabilität erheblich verbessert haben.</span><span class="sxs-lookup"><span data-stu-id="b2184-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="b2184-106">Die meisten Änderungen waren grundlegende Änderungen, die erforderlich waren, um TAPI in Windows NT 4,0 zu bringen und die Vorteile der Features zu nutzen (vollständige 32-Bit-Unterstützung, Dienste und Unicode).</span><span class="sxs-lookup"><span data-stu-id="b2184-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="b2184-107">Allerdings waren diese Änderungen intern zu TAPI und hatten nur wenig Auswirkungen auf TAPI-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b2184-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="b2184-108">Anwendungen, die TAPI 1,3 und 1,4 (16-Bit-Anwendungen über eine thunkingschicht) unterstützen, funktionieren gut für Windows Server 2003-Betriebssysteme, Windows XP, Windows 2000 und Windows NT.</span><span class="sxs-lookup"><span data-stu-id="b2184-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="b2184-109">Die Auswirkungen auf Entwickler von Dienstanbietern waren jedoch von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b2184-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="b2184-110">Dienstanbieter für diese Betriebssysteme müssen vollständige 32-Bit-Unicode-DLLs sein, die im Kontext von tapisrv ausgeführt werden können, und nicht im Kontext der TAPI-Anwendung (wie alle früheren Win16 basierten TSPS).</span><span class="sxs-lookup"><span data-stu-id="b2184-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="b2184-111">TSPS, die für TAPI 1,4 entworfen wurden, funktionieren unter Windows Server 2003-Betriebssystemen, Windows XP, Windows 2000 oder Windows NT nicht.</span><span class="sxs-lookup"><span data-stu-id="b2184-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="b2184-112">TAPI 2,0 bietet auch die wichtigen Features der Support Unterstützung für Callcenter und Quality of Service (QoS).</span><span class="sxs-lookup"><span data-stu-id="b2184-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="b2184-113">Die im Lieferumfang von Windows enthaltenen TAPI-System Binärdateien unterstützen TAPI-Versionen 1,3 und 1,4 für alle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b2184-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="b2184-114">Allerdings können von 16-Bit-Anwendungen TAPI 2,0 nicht verwendet werden, und Sie können keine 16-Bit-TAPI 2. x-TSP verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2184-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 



