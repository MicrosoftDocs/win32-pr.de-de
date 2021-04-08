---
description: In der folgenden Tabelle sind die
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Tools für Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959748"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="efd6f-103">Tools für Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="efd6f-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="efd6f-104">Tools für die Datensammlung</span><span class="sxs-lookup"><span data-stu-id="efd6f-104">Data collection tools</span></span>

<span data-ttu-id="efd6f-105">Die folgenden Tools sind hilfreich beim Verarbeiten oder Bearbeiten von Windows-Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="efd6f-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="efd6f-106">Tool</span><span class="sxs-lookup"><span data-stu-id="efd6f-106">Tool</span></span>|<span data-ttu-id="efd6f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efd6f-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="efd6f-108">Systemmonitor</span><span class="sxs-lookup"><span data-stu-id="efd6f-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="efd6f-109">GUI-Tool zum Erfassen und Anzeigen von Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="efd6f-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="efd6f-110">`perfmon.exe` Hiermit wird die MMC mit dem System Monitor-Snap-in gestartet, das Zugriff auf die Tools "System Monitor", "Datensammler Sätze" und "Berichte" bietet.</span><span class="sxs-lookup"><span data-stu-id="efd6f-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="efd6f-111">TypePerf</span><span class="sxs-lookup"><span data-stu-id="efd6f-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="efd6f-112">Befehlszeilen Tool zum Erfassen und Drucken von Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="efd6f-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="efd6f-113">Kann verwendet werden, um verfügbare Gegensätze aufzulisten, Verfügbare Leistungsindikatoren aufzulisten, Indikator Daten in der Konsole auszugeben oder Leistungsindikator Daten in einer Protokolldatei (CSV, TDF, BLG) zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="efd6f-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="efd6f-114">Relog</span><span class="sxs-lookup"><span data-stu-id="efd6f-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="efd6f-115">Befehlszeilen Tool zum Transformieren und Zusammenführen von Protokolldateien (CSV, TDF, BLG), `typeperf.exe` die über oder über die APIs aufgezeichnet wurden `PDH.dll` .</span><span class="sxs-lookup"><span data-stu-id="efd6f-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="efd6f-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="efd6f-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="efd6f-117">Befehlszeilen Tool zum Steuern von Datensammler Sätzen.</span><span class="sxs-lookup"><span data-stu-id="efd6f-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="efd6f-118">Datenanbieter Tools</span><span class="sxs-lookup"><span data-stu-id="efd6f-118">Data provider tools</span></span>

<span data-ttu-id="efd6f-119">Die folgenden Tools sind hilfreich beim Veröffentlichen von Windows-Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="efd6f-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="efd6f-120">Tool</span><span class="sxs-lookup"><span data-stu-id="efd6f-120">Tool</span></span>|<span data-ttu-id="efd6f-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efd6f-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="efd6f-122">Ctrpp</span><span class="sxs-lookup"><span data-stu-id="efd6f-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="efd6f-123">Das Befehlszeilen-Buildtool aus dem Windows SDK, das das Leistungsindikator-v2-Anbieter Manifest überprüft und kompiliert.</span><span class="sxs-lookup"><span data-stu-id="efd6f-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="efd6f-124">Dieses Tool generiert die `.h` Header und `.rc` Ressourcen Skripts, die zum Erstellen eines v2-Anbieters benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="efd6f-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="efd6f-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="efd6f-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="efd6f-126">Ein Befehlszeilen Tool, mit dem der Anbieter auf einem System installiert wird.</span><span class="sxs-lookup"><span data-stu-id="efd6f-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="efd6f-127">UnlodCtr</span><span class="sxs-lookup"><span data-stu-id="efd6f-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="efd6f-128">Ein Befehlszeilen Tool, mit dem der Anbieter von einem System deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="efd6f-128">Command-line tool used to uninstall your provider from a system.</span></span>
