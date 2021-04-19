---
description: Konfigurieren einer Medienquelle
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Konfigurieren einer Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361767"
---
# <a name="configuring-a-media-source"></a>Konfigurieren einer Medienquelle

Wenn Sie den [quellresolver](source-resolver.md) zum Erstellen einer Medienquelle verwenden, können Sie einen Eigenschaften Speicher angeben, der Konfigurations Eigenschaften enthält. Diese Eigenschaften werden verwendet, um die Medienquelle zu initialisieren. Der Satz unterstützter Eigenschaften hängt von der Implementierung der Medienquelle ab. Nicht jede Medienquelle definiert Konfigurations Eigenschaften.

In der folgenden Tabelle sind die Konfigurations Eigenschaften für die Medienquellen aufgeführt, die in Media Foundation bereitgestellt werden. Medienquellen von Drittanbietern können eigene benutzerdefinierte Eigenschaften definieren.



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
<td>Siehe <a href="network-source-features.md">Netzwerk Quell Features</a>.</td>
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



 

Führen Sie die folgenden Schritte aus, um eine Quelle zu konfigurieren.

1.  Rufen Sie **pscreatememorypropertystore** auf, um einen neuen Eigenschaften Speicher zu erstellen. Diese Funktion gibt einen **IPropertyStore** -Zeiger zurück.
2.  Aufrufen von **IPropertyStore:: SetValue** , um eine oder mehrere Konfigurations Eigenschaften festzulegen.
3.  Aufrufen einer der Erstellungs Funktionen des Quell Resolvers, wie z. b. [**imfsourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), und übergeben des **IPropertyStore** -Zeigers im *prequicparameter* .


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



Der quellresolver übergibt den **IPropertyStore** -Zeiger direkt an den Schema Handler oder den Byte Datenstrom Handler, der die Quelle erstellt. Der quellresolver versucht nicht, die Eigenschaften zu überprüfen.

Im Allgemeinen werden diese Eigenschaften für erweiterte Einstellungen verwendet. Wenn Sie keinen Eigenschaften Speicher bereitstellen, sollte die Medienquelle weiterhin ordnungsgemäß mit den Standardeinstellungen funktionieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresolver](source-resolver.md)
</dt> </dl>

 

 



