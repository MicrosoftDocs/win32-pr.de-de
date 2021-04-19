---
description: Mithilfe der Arbeitsspeicher Auslastung kann eine Direct3D-Anwendung ermitteln, wann der Arbeits Satz für den Video Arbeitsspeicher zu groß geworden ist.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Berichterstellung für Speicherauslastung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345839"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="4fb75-103">Berichterstellung für Speicherauslastung</span><span class="sxs-lookup"><span data-stu-id="4fb75-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="4fb75-104">Mithilfe der Arbeitsspeicher Auslastung kann eine Direct3D-Anwendung ermitteln, wann der Arbeits Satz für den Video Arbeitsspeicher zu groß geworden ist.</span><span class="sxs-lookup"><span data-stu-id="4fb75-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="4fb75-105">Arbeits *Speicher* Auslastung ist die Anforderung, die von einer Anwendung für das Speichersubsystem gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4fb75-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="4fb75-106">Obwohl jede Direct3D-Anwendung Arbeitsspeicher Auslastung verwenden kann, ist diese Funktion besonders nützlich für Anwendungen, die Videos mithilfe von Direct3D Rendering.</span><span class="sxs-lookup"><span data-stu-id="4fb75-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="4fb75-107">Die Video Wiedergabe bietet in der Regel große Mengen an Pufferung, sodass Frames im Voraus decodiert werden können.</span><span class="sxs-lookup"><span data-stu-id="4fb75-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="4fb75-108">Während die Pufferung in der Regel zu einer reibungsloseren Wiedergabe führt, kann die Leistung tatsächlich beeinträchtigt werden, wenn die Workingsets aufgrund der folgenden Faktoren zu groß werden:</span><span class="sxs-lookup"><span data-stu-id="4fb75-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="4fb75-109">Der Arbeitsspeicher kann aus dem Cache entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4fb75-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="4fb75-110">Im schlimmsten Fall kann dies in jedem Video Frame vorkommen.</span><span class="sxs-lookup"><span data-stu-id="4fb75-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="4fb75-111">Speicher Belegungen werden möglicherweise in nicht optimalen Speicher Segmenten platziert.</span><span class="sxs-lookup"><span data-stu-id="4fb75-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="4fb75-112">Ab Windows 7 kann Direct3D einige Statistiken über den Druck des Grafik Speichers melden:</span><span class="sxs-lookup"><span data-stu-id="4fb75-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="4fb75-113">Die Anzahl der Bytes, die vom Prozess in einem bestimmten Zeitraum entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="4fb75-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="4fb75-114">Die Menge an Arbeitsspeicher in nicht optimalen Speicher Segmenten.</span><span class="sxs-lookup"><span data-stu-id="4fb75-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="4fb75-115">Eine grobe Angabe der Gesamteffizienz der Speicher Belegungen, die im nicht optimalen Arbeitsspeicher platziert werden.</span><span class="sxs-lookup"><span data-stu-id="4fb75-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="4fb75-116">Diese Informationen können einer Anwendung helfen, einen angemessenen Arbeits Satz zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="4fb75-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="4fb75-117">Verwenden der Speicherdruck Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="4fb75-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="4fb75-118">Die Arbeitsspeicher Auslastung verwendet die vorhandene **IDirect3DQuery9** -Schnittstelle, um das Gerät abzufragen.</span><span class="sxs-lookup"><span data-stu-id="4fb75-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="4fb75-119">Der **D3DQUERYTYPE** -Enumeration wurde ein neuer Abfragetyp hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4fb75-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="4fb75-120">Führen Sie die folgenden Schritte aus, um diese Abfrage zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="4fb75-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="4fb75-121">Aufrufen von **IDirect3DDevice9Ex:: kreatequery** mit dem **D3DQUERYTYPE \_ memorypressure** -Flag.</span><span class="sxs-lookup"><span data-stu-id="4fb75-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="4fb75-122">Diese Methode gibt einen Zeiger auf die **IDirect3DQuery9** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4fb75-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="4fb75-123">Wenden Sie **IDirect3DQuery9:: Issue** mit dem **D3DISSUE \_ Begin** -Flag an, um das Mess Intervall zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="4fb75-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="4fb75-124">Nennen Sie **IDirect3DQuery9:: Issue** mit dem **D3DISSUE \_ End** -Flag.</span><span class="sxs-lookup"><span data-stu-id="4fb75-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="4fb75-125">Aufrufen von **IDirect3DQuery9:: GetData** , um das Abfrageergebnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fb75-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="4fb75-126">Die Abfrage gibt eine [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="4fb75-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="4fb75-127">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="4fb75-127">Example Code</span></span>

<span data-ttu-id="4fb75-128">Das folgende Beispiel zeigt zwei Funktionen, die Arbeitsspeicher Auslastung messen.</span><span class="sxs-lookup"><span data-stu-id="4fb75-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="4fb75-129">Der erste beginnt mit dem Mess Intervall, und der zweite Ruft die Ergebnisse der Messung ab.</span><span class="sxs-lookup"><span data-stu-id="4fb75-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4fb75-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fb75-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fb75-131">Direct3D-Video-APIs</span><span class="sxs-lookup"><span data-stu-id="4fb75-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



