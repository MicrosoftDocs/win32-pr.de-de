---
description: 'Leistungsdaten können mit einer der folgenden Schnittstellen genutzt werden: der PDH-Schnittstelle (Performance Data Helper), die einen Zugriff auf hoher Ebene auf Daten von den Leistungs Anbieter Anbietern der Version 1 und der Version 2 ermöglicht. Die Registrierungs Schnittstelle, die einen Low-Level-Zugriff auf Daten von leistungsindikatorenanbietern ermöglicht. Die Leistungs Bibliotheks Schnittstelle, die den direkten Zugriff auf Daten von Leistungs Anbieter Anbietern der Version 2 ermöglicht. Die PDH-Schnittstelle ist einfacher zu verwenden als die Registrierungs Schnittstelle und wird für die meisten Leistungsdaten Sammlungs Aufgaben empfohlen. Die PDH-Schnittstelle ist im Wesentlichen eine Abstraktions Ebene der Funktionalität, die die Registrierungs Schnittstelle bereitstellt. Verwenden Sie die Schnittstelle der Leistungs Bibliothek nur, wenn Sie die PDH-Abstraktions Ebenenfunktionen nicht verwenden können.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Verarbeiten von Counter-Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353462"
---
# <a name="consuming-counter-data"></a><span data-ttu-id="01bb7-105">Verarbeiten von Counter-Daten</span><span class="sxs-lookup"><span data-stu-id="01bb7-105">Consuming Counter Data</span></span>

<span data-ttu-id="01bb7-106">Programme, die Windows-Leistungsdaten des Leistungs Zählers lesen und verwenden möchten, können je nach Szenario eine von mehreren Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="01bb7-106">Programs that want to read and make use of Windows Performance Counter data can use one of several interfaces as appropriate for the scenario.</span></span>

- <span data-ttu-id="01bb7-107">Skripts können die [WMI-Leistungs Leistungswert Klassen](/windows/desktop/WmiSdk/monitoring-performance-data) oder das [typeperf](/windows-server/administration/windows-commands/typeperf) -Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="01bb7-107">Scripts can use the [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) or the [TypePerf](/windows-server/administration/windows-commands/typeperf) tool.</span></span>
- <span data-ttu-id="01bb7-108">.Net-Programme können die [Performance Counter-Klasse](/dotnet/api/system.diagnostics.performancecounter)verwenden.</span><span class="sxs-lookup"><span data-stu-id="01bb7-108">.NET programs can use the [PerformanceCounter Class](/dotnet/api/system.diagnostics.performancecounter).</span></span>
- <span data-ttu-id="01bb7-109">Die [PDH-Bibliothek (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) bietet über eine Win32-API (C/C++) Zugriff auf hoher Ebene auf Daten von v1-und v2-Leistungs Anbieter</span><span class="sxs-lookup"><span data-stu-id="01bb7-109">The [Performance Data Helper (PDH) library](using-the-pdh-functions-to-consume-counter-data.md) provides high-level access to data from both V1 and V2 performance counter providers via a Win32 (C/C++) API.</span></span>
- <span data-ttu-id="01bb7-110">Die [Registrierungs Schnittstelle](using-the-registry-functions-to-consume-counter-data.md) ermöglicht den Zugriff auf Daten von v1-und v2-leistungsindikatorenanbietern über den speziellen `HKEY_PERFORMANCE_DATA` Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="01bb7-110">The [registry interface](using-the-registry-functions-to-consume-counter-data.md) provides access to data from both V1 and V2 performance counter providers via the special `HKEY_PERFORMANCE_DATA` registry key.</span></span>
- <span data-ttu-id="01bb7-111">Die leistungsfähigen [Funktionen von Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) bieten über eine Win32-API (C/C++) einen Low-Level-Zugriff auf Daten von V2-Leistungs Anbieter-Anbietern.</span><span class="sxs-lookup"><span data-stu-id="01bb7-111">The [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) provide low-level access to data from V2 performance counter providers via a Win32 (C/C++) API.</span></span>

<span data-ttu-id="01bb7-112">Die PDH-Schnittstelle wird für die meisten C/C++-Leistungsdaten Sammlungs Aufgaben empfohlen, da Sie einfacher zu verwenden ist als die Registrierungs-und Perflib-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="01bb7-112">The PDH interface is recommended for most C/C++ performance data collection tasks because it is easier to use than the registry and PerfLib interfaces.</span></span>
