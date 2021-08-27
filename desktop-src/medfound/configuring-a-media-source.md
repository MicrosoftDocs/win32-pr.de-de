---
description: Konfigurieren einer Medienquelle
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Konfigurieren einer Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 809d215cf282dba1e65c21316fafda47684a2151
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481706"
---
# <a name="configuring-a-media-source"></a>Konfigurieren einer Medienquelle

Wenn Sie den [Quell resolver](source-resolver.md) verwenden, um eine Medienquelle zu erstellen, können Sie einen Eigenschaftenspeicher angeben, der Konfigurationseigenschaften enthält. Diese Eigenschaften werden verwendet, um die Medienquelle zu initialisieren. Der Satz der unterstützten Eigenschaften hängt von der Implementierung der Medienquelle ab. Nicht jede Medienquelle definiert Konfigurationseigenschaften.

In der folgenden Tabelle sind die Konfigurationseigenschaften für die Medienquellen aufgeführt, die in Media Foundation bereitgestellt werden. Medienquellen von Drittanbietern können eigene benutzerdefinierte Eigenschaften definieren.




| Medienquelle | Eigenschaften | 
|--------------|------------|
| Netzwerkquelle | Weitere Informationen finden Sie unter <a href="network-source-features.md">Netzwerkquellfeatures.</a> | 
| ASF-Medienquelle | <ul><li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li><li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li></ul> | 




 

Führen Sie die folgenden Schritte aus, um eine Quelle zu konfigurieren.

1.  Rufen Sie **PSCreateMemoryPropertyStore** auf, um einen neuen Eigenschaftenspeicher zu erstellen. Diese Funktion gibt einen **IPropertyStore-Zeiger** zurück.
2.  Rufen Sie **IPropertyStore::SetValue** auf, um eine oder mehrere Konfigurationseigenschaften festzulegen.
3.  Rufen Sie eine der Erstellungsfunktionen des Quellresolvers auf, wie z. [**B. EINENSOURCEResolver::CreateObjectFromURL,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)und übergeben Sie den **IPropertyStore-Zeiger** im *pProps-Parameter.*


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



Der Quell resolver übergibt den **IPropertyStore-Zeiger** direkt an den Schemahandler oder byte-stream-Handler, der die Quelle erstellt. Der Quell resolver versucht nicht, die Eigenschaften zu überprüfen.

Im Allgemeinen werden diese Eigenschaften für erweiterte Einstellungen verwendet. Wenn Sie keinen Eigenschaftenspeicher bereitstellen, sollte die Medienquelle weiterhin ordnungsgemäß mit Standardeinstellungen funktionieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quelllöser](source-resolver.md)
</dt> </dl>

 

 



