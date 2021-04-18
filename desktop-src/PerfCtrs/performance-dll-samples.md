---
description: Die Windows SDK (WSDK) enthält drei komplette Leistungs-DLLs für Stichproben.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Leistungs-DLL-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358894"
---
# <a name="performance-dll-samples"></a><span data-ttu-id="7188c-103">Leistungs-DLL-Beispiele</span><span class="sxs-lookup"><span data-stu-id="7188c-103">Performance DLL Samples</span></span>

<span data-ttu-id="7188c-104">Die Windows SDK (WSDK) enthält drei komplette Leistungs-DLLs für Stichproben.</span><span class="sxs-lookup"><span data-stu-id="7188c-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="7188c-105">Diese Beispiele befinden sich im Verzeichnis Samples \\ Winbase \\ Winnt \\ perftool \\ perfdlls.</span><span class="sxs-lookup"><span data-stu-id="7188c-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="7188c-106">Der Stamm dieses Pfades ist das Basis Installationsverzeichnis des WSDK.</span><span class="sxs-lookup"><span data-stu-id="7188c-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="7188c-107">Sie können das WSDK aus dem [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) herunterladen (suchen Sie nach Windows SDK, und wählen Sie den Download für das neueste veröffentlichte Betriebssystem aus).</span><span class="sxs-lookup"><span data-stu-id="7188c-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="7188c-108">Die in diesem Verzeichnis enthaltenen Beispiele sind:</span><span class="sxs-lookup"><span data-stu-id="7188c-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="7188c-109">**Appmem**– stellt Entsprechungen der Funktionen [**globalzugewiesenen**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**globalrezuweisung**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)und [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) bereit, die Leistungsinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="7188c-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="7188c-110">Leistungsindikatoren in der Registrierung und das Leistungs Tool können die Leistungsinformationen lesen.</span><span class="sxs-lookup"><span data-stu-id="7188c-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="7188c-111">" **Leakybin**–" veranschaulicht die Verwendung von Leistungsindikatoren für Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7188c-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="7188c-112">**Perfgen**– bietet drei Wellenformen in fünf verschiedenen Zeiträumen für die Verwendung mit dem Leistungs Tool, um Daten mit einer bekannten Geschwindigkeit und einem bekannten Wert bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7188c-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="7188c-113">Dies kann nützlich sein, um Anwendungen zu testen, die Leistungsdaten verwenden und vorhersagbare Werte für den Test benötigen.</span><span class="sxs-lookup"><span data-stu-id="7188c-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
