---
description: Mit der Berichterstellung für hohe Arbeitsspeicherauslastung kann eine Direct3D-Anwendung ermitteln, wann ihr Videoarbeitssatz zu groß geworden ist.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Berichterstellung zu Auslastung des Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dc0df8db30281c6f7225309bdca5edfdbd3759f21a9e61cdc848f534dcce41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723770"
---
# <a name="memory-pressure-reporting"></a>Berichterstellung zu Auslastung des Arbeitsspeichers

Mit der Berichterstellung für hohe Arbeitsspeicherauslastung kann eine Direct3D-Anwendung ermitteln, wann ihr Videoarbeitssatz zu groß geworden ist.

*Arbeitsspeicherauslastung* ist die Anforderung, die von einer Anwendung auf das Speichersubsystem gestellt wird. Während jede Direct3D-Anwendung berichte zu arbeitsspeicherauslastungen verwenden kann, ist dieses Feature besonders nützlich für Anwendungen, die Videos mithilfe von Direct3D rendern. Die Videowiedergabe profitiert in der Regel von großen Mengen an Pufferung, sodass Frames im Voraus decodiert werden können. Die Pufferung führt in der Regel zu einer reibungsloseren Wiedergabe, kann jedoch die Leistung beeinträchtigen, wenn das Arbeitsset aufgrund der folgenden Faktoren zu groß wird:

-   Der Arbeitsspeicher kann aus dem Cache entfernt werden. Im schlimmsten Fall kann dies auf jedem Videoframe auftreten.
-   Speicherbelegungen können in nicht optimalen Speichersegmenten platziert werden.

Ab Windows 7 kann Direct3D einige Statistiken zur Auslastung des Videospeichers melden:

-   Die Anzahl der Bytes, die vom Prozess in einem Zeitintervall entfernt wurden.
-   Die Menge an Arbeitsspeicher, die in nicht optimalen Speichersegmenten platziert wird.
-   Ein grober Hinweis auf die Gesamteffizienz der Speicherbelegungen im nicht optimalen Speicher.

Diese Informationen können einer Anwendung helfen, einen angemessenen Arbeitssatz zu verwalten.

## <a name="using-memory-pressure-reporting"></a>Verwenden der Speicherauslastungsberichterstellung

Die Speicherauslastungsberichterstellung verwendet die vorhandene **IDirect3DQuery9-Schnittstelle,** um das Gerät abzufragen. Der **D3DQUERYTYPE-Enumeration** wurde ein neuer Abfragetyp hinzugefügt.


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Führen Sie die folgenden Schritte aus, um diese Abfrage zu verwenden:

1.  Rufen Sie **IDirect3DDevice9Ex::CreateQuery** mit dem **Flag D3DQUERYTYPE \_ MEMORYPRESSURE** auf. Diese Methode gibt einen Zeiger auf die **IDirect3DQuery9-Schnittstelle** zurück.
2.  Rufen Sie **IDirect3DQuery9::Issue** mit dem **D3DISSUE \_ BEGIN-Flag** auf, um das Messintervall zu starten.
3.  Rufen Sie **IDirect3DQuery9::Issue** mit dem **D3DISSUE \_ END-Flag** auf.
4.  Rufen Sie **IDirect3DQuery9::GetData** auf, um das Abfrageergebnis abzurufen. Die Abfrage gibt eine [**D3DMEMORYPRESSURE-Struktur**](d3dmemorypressure.md) zurück.

## <a name="example-code"></a>Beispielcode

Das folgende Beispiel zeigt zwei Funktionen, die die Arbeitsspeicherauslastung messen. Die erste beginnt mit dem Messintervall, und die zweite ruft die Ergebnisse der Messung ab.


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

[Direct3D Video-APIs](direct3d-video-apis.md)
</dt> </dl>

 

 



