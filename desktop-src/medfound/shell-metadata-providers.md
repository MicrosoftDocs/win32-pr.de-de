---
description: Ab Windows 7 macht Microsoft Media Foundation Metadaten über die IPropertyStore-Schnittstelle verfügbar.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Shellmetadatenanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353172"
---
# <a name="shell-metadata-providers"></a><span data-ttu-id="8486d-103">Shellmetadatenanbieter</span><span class="sxs-lookup"><span data-stu-id="8486d-103">Shell Metadata Providers</span></span>

<span data-ttu-id="8486d-104">Ab Windows 7 macht Microsoft Media Foundation Metadaten über die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8486d-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="8486d-105">Metadaten, die mit dem in diesem Thema definierten Prozess abgerufen werden, sollten nur für den schreibgeschützten Zugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8486d-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="8486d-106">Das Schreiben von Daten mit diesem Prozess wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8486d-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="8486d-107">Sie können ein [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekt zu Schreib Zwecken mithilfe eines Klassen Bezeichners (CLSID) erstellen, der von [**pslookuppropertyhandlerclsid**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8486d-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="8486d-108">Lesen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="8486d-108">Reading Metadata</span></span>

<span data-ttu-id="8486d-109">Um Metadaten aus einer Medienquelle zu lesen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8486d-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="8486d-110">Einen Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="8486d-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="8486d-111">Sie können die [**imfsourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstelle verwenden, um einen **imfmediasource** -Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8486d-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="8486d-112">Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für die Medienquelle, um einen Zeiger auf die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8486d-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="8486d-113">Geben Sie im *guidservice* -Parameter von **MF-Service** den Wert **MF- \_ eigenschaftenhandlerdienst \_ \_** an.</span><span class="sxs-lookup"><span data-stu-id="8486d-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="8486d-114">Wenn die Quelle die **IPropertyStore** -Schnittstelle nicht unterstützt, gibt **MF-Service** einen **\_ \_ nicht \_ unterstützten MF-Dienst** zurück.</span><span class="sxs-lookup"><span data-stu-id="8486d-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="8486d-115">Aufrufen von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Methoden zum Aufzählen der Metadateneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8486d-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="8486d-116">Der folgende Code zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="8486d-116">The following code shows these steps.</span></span> <span data-ttu-id="8486d-117">Angenommen, `DisplayProperty` Es handelt sich um eine Funktion, die einen **PROPVARIANT** -Wert anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8486d-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



<span data-ttu-id="8486d-118">Eine Liste der Metadaten-Eigenschafts Schlüssel finden Sie unter [Metadateneigenschaften für Mediendateien](metadata-properties-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="8486d-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8486d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8486d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8486d-120">Medien Metadaten</span><span class="sxs-lookup"><span data-stu-id="8486d-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
