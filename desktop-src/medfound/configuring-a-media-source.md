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
# <a name="configuring-a-media-source"></a><span data-ttu-id="8de21-103">Konfigurieren einer Medienquelle</span><span class="sxs-lookup"><span data-stu-id="8de21-103">Configuring a Media Source</span></span>

<span data-ttu-id="8de21-104">Wenn Sie den [quellresolver](source-resolver.md) zum Erstellen einer Medienquelle verwenden, können Sie einen Eigenschaften Speicher angeben, der Konfigurations Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="8de21-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="8de21-105">Diese Eigenschaften werden verwendet, um die Medienquelle zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8de21-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="8de21-106">Der Satz unterstützter Eigenschaften hängt von der Implementierung der Medienquelle ab.</span><span class="sxs-lookup"><span data-stu-id="8de21-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="8de21-107">Nicht jede Medienquelle definiert Konfigurations Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8de21-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="8de21-108">In der folgenden Tabelle sind die Konfigurations Eigenschaften für die Medienquellen aufgeführt, die in Media Foundation bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8de21-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="8de21-109">Medienquellen von Drittanbietern können eigene benutzerdefinierte Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="8de21-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8de21-110">Medienquelle</span><span class="sxs-lookup"><span data-stu-id="8de21-110">Media source</span></span></th>
<th><span data-ttu-id="8de21-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8de21-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8de21-112">Netzwerkquelle</span><span class="sxs-lookup"><span data-stu-id="8de21-112">Network source</span></span></td>
<td><span data-ttu-id="8de21-113">Siehe <a href="network-source-features.md">Netzwerk Quell Features</a>.</span><span class="sxs-lookup"><span data-stu-id="8de21-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8de21-114">ASF-Medienquelle</span><span class="sxs-lookup"><span data-stu-id="8de21-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="8de21-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="8de21-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="8de21-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="8de21-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="8de21-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="8de21-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="8de21-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="8de21-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8de21-119">Führen Sie die folgenden Schritte aus, um eine Quelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8de21-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="8de21-120">Rufen Sie **pscreatememorypropertystore** auf, um einen neuen Eigenschaften Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8de21-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="8de21-121">Diese Funktion gibt einen **IPropertyStore** -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="8de21-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="8de21-122">Aufrufen von **IPropertyStore:: SetValue** , um eine oder mehrere Konfigurations Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8de21-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="8de21-123">Aufrufen einer der Erstellungs Funktionen des Quell Resolvers, wie z. b. [**imfsourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), und übergeben des **IPropertyStore** -Zeigers im *prequicparameter* .</span><span class="sxs-lookup"><span data-stu-id="8de21-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


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



<span data-ttu-id="8de21-124">Der quellresolver übergibt den **IPropertyStore** -Zeiger direkt an den Schema Handler oder den Byte Datenstrom Handler, der die Quelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="8de21-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="8de21-125">Der quellresolver versucht nicht, die Eigenschaften zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8de21-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="8de21-126">Im Allgemeinen werden diese Eigenschaften für erweiterte Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8de21-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="8de21-127">Wenn Sie keinen Eigenschaften Speicher bereitstellen, sollte die Medienquelle weiterhin ordnungsgemäß mit den Standardeinstellungen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="8de21-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de21-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8de21-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de21-129">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="8de21-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



