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
# <a name="memory-pressure-reporting"></a>Berichterstellung für Speicherauslastung

Mithilfe der Arbeitsspeicher Auslastung kann eine Direct3D-Anwendung ermitteln, wann der Arbeits Satz für den Video Arbeitsspeicher zu groß geworden ist.

Arbeits *Speicher* Auslastung ist die Anforderung, die von einer Anwendung für das Speichersubsystem gestellt wird. Obwohl jede Direct3D-Anwendung Arbeitsspeicher Auslastung verwenden kann, ist diese Funktion besonders nützlich für Anwendungen, die Videos mithilfe von Direct3D Rendering. Die Video Wiedergabe bietet in der Regel große Mengen an Pufferung, sodass Frames im Voraus decodiert werden können. Während die Pufferung in der Regel zu einer reibungsloseren Wiedergabe führt, kann die Leistung tatsächlich beeinträchtigt werden, wenn die Workingsets aufgrund der folgenden Faktoren zu groß werden:

-   Der Arbeitsspeicher kann aus dem Cache entfernt werden. Im schlimmsten Fall kann dies in jedem Video Frame vorkommen.
-   Speicher Belegungen werden möglicherweise in nicht optimalen Speicher Segmenten platziert.

Ab Windows 7 kann Direct3D einige Statistiken über den Druck des Grafik Speichers melden:

-   Die Anzahl der Bytes, die vom Prozess in einem bestimmten Zeitraum entfernt wurden.
-   Die Menge an Arbeitsspeicher in nicht optimalen Speicher Segmenten.
-   Eine grobe Angabe der Gesamteffizienz der Speicher Belegungen, die im nicht optimalen Arbeitsspeicher platziert werden.

Diese Informationen können einer Anwendung helfen, einen angemessenen Arbeits Satz zu verwalten.

## <a name="using-memory-pressure-reporting"></a>Verwenden der Speicherdruck Berichterstattung

Die Arbeitsspeicher Auslastung verwendet die vorhandene **IDirect3DQuery9** -Schnittstelle, um das Gerät abzufragen. Der **D3DQUERYTYPE** -Enumeration wurde ein neuer Abfragetyp hinzugefügt.


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Führen Sie die folgenden Schritte aus, um diese Abfrage zu verwenden:

1.  Aufrufen von **IDirect3DDevice9Ex:: kreatequery** mit dem **D3DQUERYTYPE \_ memorypressure** -Flag. Diese Methode gibt einen Zeiger auf die **IDirect3DQuery9** -Schnittstelle zurück.
2.  Wenden Sie **IDirect3DQuery9:: Issue** mit dem **D3DISSUE \_ Begin** -Flag an, um das Mess Intervall zu beginnen.
3.  Nennen Sie **IDirect3DQuery9:: Issue** mit dem **D3DISSUE \_ End** -Flag.
4.  Aufrufen von **IDirect3DQuery9:: GetData** , um das Abfrageergebnis zu erhalten. Die Abfrage gibt eine [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) -Struktur zurück.

## <a name="example-code"></a>Beispielcode

Das folgende Beispiel zeigt zwei Funktionen, die Arbeitsspeicher Auslastung messen. Der erste beginnt mit dem Mess Intervall, und der zweite Ruft die Ergebnisse der Messung ab.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Video-APIs](direct3d-video-apis.md)
</dt> </dl>

 

 



