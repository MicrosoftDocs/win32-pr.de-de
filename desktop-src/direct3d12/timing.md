---
title: Zeitliche Steuerung (Direct3D 12-Grafiken)
description: In diesem Abschnitt wird das Abfragen von Zeitstempeln und das Kalibrieren der GPU-und CPU-Zeitstempelzähler behandelt.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548753"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="4f445-103">Zeitliche Steuerung (Direct3D 12-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="4f445-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="4f445-104">In diesem Abschnitt wird das Abfragen von Zeitstempeln und das Kalibrieren der GPU-und CPU-Zeitstempelzähler behandelt.</span><span class="sxs-lookup"><span data-stu-id="4f445-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="4f445-105">Zeitstempel Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="4f445-105">Timestamp frequency</span></span>

<span data-ttu-id="4f445-106">Die Anwendung kann die GPU-Zeitstempel Häufigkeit pro Befehls Warteschlange Abfragen (Weitere Informationen finden Sie in der [**ID3D12CommandQueue:: gettimestampfrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) -Methode).</span><span class="sxs-lookup"><span data-stu-id="4f445-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="4f445-107">Die zurückgegebene Häufigkeit wird in Hz (Ticks/Sek.) gemessen.</span><span class="sxs-lookup"><span data-stu-id="4f445-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="4f445-108">Wenn die angegebene Befehls Warteschlange keine Zeitstempel unterstützt (siehe die Tabelle im Abschnitt " [Abfragen](queries.md) "), schlägt diese API fehl (und gibt **E_FAIL** zurück).</span><span class="sxs-lookup"><span data-stu-id="4f445-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="4f445-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) und [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) unterstützen stets Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="4f445-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="4f445-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optional Zeitstempel unterstützt, wenn der [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: copyqueuetimestampqueriessupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) -Member " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="4f445-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="4f445-111">Zeitstempel-Kalibrierung</span><span class="sxs-lookup"><span data-stu-id="4f445-111">Timestamp calibration</span></span>

<span data-ttu-id="4f445-112">D3D12 ermöglicht Anwendungen das korrelieren von Ergebnissen, die von Zeitstempel-Abfragen abgerufen wurden, mit Ergebnissen, die durch `QueryPerformanceCounter` den Aufruf</span><span class="sxs-lookup"><span data-stu-id="4f445-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="4f445-113">Dies wird durch den Aufrufen von [**ID3D12CommandQueue:: getclockkalibrierung**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4f445-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="4f445-114">[**Getclockkalibrierung**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) erfasst den GPU-Zeitstempel-Counter für eine bestimmte Befehls Warteschlange und erfasst den CPU-Wert über `QueryPerformanceCounter` nahezu zur gleichen Zeit.</span><span class="sxs-lookup"><span data-stu-id="4f445-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="4f445-115">Auch diese API schlägt fehl (bei Rückgabe von E \_ Fail), wenn die angegebene Befehls Warteschlange keine Zeitstempel unterstützt (siehe Tabelle im Thema [Abfragen](queries.md) ).</span><span class="sxs-lookup"><span data-stu-id="4f445-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="4f445-116">Beachten Sie, dass GPU-und CPU-Zeitstempel-Indikatoren nicht notwendigerweise direkt mit der Taktfrequenz dieser Prozessoren in Zusammenhang stehen, sondern von Zeitstempel Ticks arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4f445-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="4f445-117">Timestamp-Abfragen</span><span class="sxs-lookup"><span data-stu-id="4f445-117">Timestamp queries</span></span>

<span data-ttu-id="4f445-118">Sie können Zeitstempel als Teil einer Befehlsliste (anstelle eines CPU-seitigen Aufrufes Aufrufes in einer Befehls Warteschlange) über Zeitstempel-Abfragen abrufen.</span><span class="sxs-lookup"><span data-stu-id="4f445-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="4f445-119">(Weitere Informationen zu Abfragen im Allgemeinen finden Sie unter [Abfragen](queries.md) .)</span><span class="sxs-lookup"><span data-stu-id="4f445-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="4f445-120">Alle Zeitstempel-Abfragen verwenden den Type- [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) für die eigentliche Abfrage.</span><span class="sxs-lookup"><span data-stu-id="4f445-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="4f445-121">Aufgrund von Hardwarebeschränkungen verwenden [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) und [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) jedoch einen anderen [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) als den, der von [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f445-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="4f445-122">Direct-und Compute-Warteschlangen verwenden [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="4f445-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="4f445-123">Kopier Warteschlangen verwenden [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="4f445-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="4f445-124">Abfragen zum Kopieren von Warteschlangen werden nur unterstützt, wenn der [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: copyqueuetimestampqueriessupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) -Member " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="4f445-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="4f445-125">Timestamp-Abfragen, die über [**ID3D12GraphicsCommandList:: resolvequerydata**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)aufgelöst werden, sind ein **UINT64** , das Ticks darstellt, wie von [**ID3D12CommandQueue:: getclockkalibrierung**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)zurückgegeben, und daher muss Sie durch die Warteschlangen Häufigkeit geteilt werden, um die Länge in Sekunden zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4f445-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f445-126">Verwenden Sie aus Gründen der Genauigkeit beim Berechnen der Sekunden-oder millisekundenintervalle von Zeitstempeln Gleit Komma Arithmetik.</span><span class="sxs-lookup"><span data-stu-id="4f445-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="4f445-127">Verwenden Sie z. B. `queriedTicks / (double)Frequency` statt `queriedTicks / Frequency`.</span><span class="sxs-lookup"><span data-stu-id="4f445-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f445-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4f445-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f445-129">Zähler und Abfragen</span><span class="sxs-lookup"><span data-stu-id="4f445-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="4f445-130">**ID3D12Device:: setstablepowerstate**</span><span class="sxs-lookup"><span data-stu-id="4f445-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="4f445-131">**ID3D12Object:: SetName**</span><span class="sxs-lookup"><span data-stu-id="4f445-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="4f445-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="4f445-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="4f445-133">Leistungsmessung</span><span class="sxs-lookup"><span data-stu-id="4f445-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>
