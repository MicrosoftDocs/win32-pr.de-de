---
description: Konfigurieren einer Medienquelle
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Konfigurieren einer Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e6737d643db2ee473214586cd7ded4f9596133dac5f4fb177df4d7b6b19757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880591"
---
# <a name="configuring-a-media-source"></a>Konfigurieren einer Medienquelle

Wenn Sie den [Quellre konfliktlöser verwenden,](source-resolver.md) um eine Medienquelle zu erstellen, können Sie einen Eigenschaftenspeicher angeben, der Konfigurationseigenschaften enthält. Diese Eigenschaften werden verwendet, um die Medienquelle zu initialisieren. Der Satz unterstützter Eigenschaften hängt von der Implementierung der Medienquelle ab. Nicht jede Medienquelle definiert Konfigurationseigenschaften.

In der folgenden Tabelle sind die Konfigurationseigenschaften für die Medienquellen aufgeführt, die in der Media Foundation. Medienquellen von Drittanbietern können eigene benutzerdefinierte Eigenschaften definieren.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Medienquelle</th>
<th>Eigenschaften</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Netzwerkquelle</td>
<td>Weitere Informationen <a href="network-source-features.md">finden Sie unter Netzwerkquellenfeatures.</a></td>
</tr>
<tr class="even">
<td>ASF-Medienquelle</td>
<td><ul>
<li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li>
<li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Führen Sie zum Konfigurieren einer Quelle die folgenden Schritte aus.

1.  Rufen **Sie PSCreateMemoryPropertyStore auf,** um einen neuen Eigenschaftenspeicher zu erstellen. Diese Funktion gibt einen **IPropertyStore-Zeiger** zurück.
2.  Rufen **Sie IPropertyStore::SetValue auf,** um eine oder mehrere Konfigurationseigenschaften festlegen.
3.  Rufen Sie eine der Erstellungsfunktionen des Quellresolvers auf, wie z.B. [**DIE QUELLQUELLEResolver::CreateObjectFromURL,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)und übergeben Sie den **IPropertyStore-Zeiger** im *pProps-Parameter.*


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Der Quellre resolver übergibt den **IPropertyStore-Zeiger** direkt an den Schemahandler oder bytestream-Handler, der die Quelle erstellt. Der Quellre resolver versucht nicht, die Eigenschaften zu überprüfen.

Im Allgemeinen werden diese Eigenschaften für erweiterte Einstellungen verwendet. Wenn Sie keinen Eigenschaftenspeicher bereitstellen, sollte die Medienquelle weiterhin ordnungsgemäß mit Standardeinstellungen funktionieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellre resolver](source-resolver.md)
</dt> </dl>

 

 



