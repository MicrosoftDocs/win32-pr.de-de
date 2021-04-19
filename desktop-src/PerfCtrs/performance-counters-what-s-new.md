---
description: In diesem Abschnitt werden die neuen Features beschrieben, die Leistungsindikatoren für die einzelnen Releases hinzugefügt wurden.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Neuerungen (Leistungsindikatoren)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348012"
---
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="b30ca-103">Neuerungen bei Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="b30ca-103">What's New with Performance Counters</span></span>

<span data-ttu-id="b30ca-104">In diesem Abschnitt werden die neuen Features beschrieben, die Leistungsindikatoren für die einzelnen Releases hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b30ca-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="b30ca-105">Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b30ca-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="b30ca-106">Das [ctrpp](ctrpp.md) -Tool wurde geändert, um die Codegenerierung zu verbessern und zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b30ca-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="b30ca-107">Das Tool generiert nun nur eine Kopfzeile und eine Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="b30ca-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="b30ca-108">Wenn Sie das alte Code Generierungs Verhalten (nicht empfohlen) verwenden möchten, können Sie das neue `-legacy` Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="b30ca-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="b30ca-109">Sie müssen jetzt das neue `-o` -Argument und das- `-rc` Argument angeben, die den Namen und den Speicherort des Headers bzw. der Ressourcen Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="b30ca-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="b30ca-110">Sie können das optionale New- `-prefix` Argument verwenden, um eine Zeichenfolge anzugeben, die dem Anfang globaler Variablen und Funktionen hinzugefügt werden soll, die in der generierten Header Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b30ca-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="b30ca-111">Wenn Sie das Zähler Manifest aktualisieren müssen, entfällt die Verwendung der neuen Codegenerierung darauf, dass Sie die vorherige Rückruf Implementierung mit dem neuen generierten Code zusammenführen müssen, da die Rückrufe nicht mehr im generierten Code enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b30ca-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="b30ca-112">Ein neues `symbol` Attribut ist für die folgenden Manifest-Elemente verfügbar:</span><span class="sxs-lookup"><span data-stu-id="b30ca-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="b30ca-113">ab</span><span class="sxs-lookup"><span data-stu-id="b30ca-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="b30ca-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="b30ca-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="b30ca-115">Indikator</span><span class="sxs-lookup"><span data-stu-id="b30ca-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="b30ca-116">Das- `symbol` Attribut ist für den [Anbieter](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) und [CounterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)erforderlich, und ist für [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)optional.</span><span class="sxs-lookup"><span data-stu-id="b30ca-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="b30ca-117">Mithilfe des-Attributs können Sie einen symbolischen Namen bereitstellen, mit dem Sie auf jedes Element verweisen können, wenn Sie die Anbieter Funktionen aufrufen (Sie können z. b. den symbolischen Namen des Leistungs Zählers beim Aufrufen von [perfcreateinstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)verwenden).</span><span class="sxs-lookup"><span data-stu-id="b30ca-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="b30ca-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b30ca-118">Windows Vista</span></span>

<span data-ttu-id="b30ca-119">Die Leistungsindikator Architektur für die Bereitstellung von Indikator Daten wurde für diese Version vollständig geändert.</span><span class="sxs-lookup"><span data-stu-id="b30ca-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="b30ca-120">Zuvor haben Sie eine INI-Datei verwendet, um die Leistungsdaten zu definieren, und Sie haben eine Leistungs-dll implementiert, die im Prozess des Consumers ausgeführt wurde, um die Daten anzugeben, wenn ein Consumer Sie angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="b30ca-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="b30ca-121">Diese Architektur ist veraltet und wird aufgrund erheblicher Leistungs-und Zuverlässigkeitsprobleme nicht für neuen Code empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b30ca-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="b30ca-122">In der neuen Architektur wird ein Manifest verwendet, um die zählungdaten zu definieren und Code im Prozess des Anbieters ausführen, um die Daten bereitzustellen, wenn ein Consumer Sie anfordert.</span><span class="sxs-lookup"><span data-stu-id="b30ca-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="b30ca-123">Weitere Informationen finden Sie unter [Bereitstellen von Counter-Daten mit Version 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="b30ca-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="b30ca-124">Die folgenden Funktionen wurden für diese Version hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="b30ca-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="b30ca-125">Controlcallback</span><span class="sxs-lookup"><span data-stu-id="b30ca-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="b30ca-126">Perfkreateingestance</span><span class="sxs-lookup"><span data-stu-id="b30ca-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="b30ca-127">Perfdelta eteinstance</span><span class="sxs-lookup"><span data-stu-id="b30ca-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="b30ca-128">Perfqueryinstance</span><span class="sxs-lookup"><span data-stu-id="b30ca-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="b30ca-129">Perfsetcountersetinfo</span><span class="sxs-lookup"><span data-stu-id="b30ca-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="b30ca-130">Perfsetulongcountervalue</span><span class="sxs-lookup"><span data-stu-id="b30ca-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="b30ca-131">Perfsetulonglongcountervalue</span><span class="sxs-lookup"><span data-stu-id="b30ca-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="b30ca-132">Perfsetcounterref-Wert</span><span class="sxs-lookup"><span data-stu-id="b30ca-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="b30ca-133">Perfstartprovider</span><span class="sxs-lookup"><span data-stu-id="b30ca-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="b30ca-134">Perfstopprovider</span><span class="sxs-lookup"><span data-stu-id="b30ca-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="b30ca-135">Die folgenden Strukturen wurden für diese Version hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="b30ca-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="b30ca-136">Identität des Leistungs \_ Zählers \_</span><span class="sxs-lookup"><span data-stu-id="b30ca-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="b30ca-137">Leistungsdaten \_ gegen \_ Info</span><span class="sxs-lookup"><span data-stu-id="b30ca-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="b30ca-138">Leistungsindikator \_ \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="b30ca-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="b30ca-139">Perf- \_ CounterSet- \_ Instanz</span><span class="sxs-lookup"><span data-stu-id="b30ca-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="b30ca-140">Eine Liste der XML-Elemente, die Sie im Manifest zum Definieren der [Leistungsindikatoren](performance-counters-schema.md)verwenden, finden Sie unter Leistungsindikator Schema.</span><span class="sxs-lookup"><span data-stu-id="b30ca-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="b30ca-141">Informationen zum ctrpp-Präprozessortool, das das Manifest analysiert und den Code generiert, den Sie als Ausgangspunkt für Ihren Anbieter verwenden, finden Sie unter [ctrpp](ctrpp.md).</span><span class="sxs-lookup"><span data-stu-id="b30ca-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>
