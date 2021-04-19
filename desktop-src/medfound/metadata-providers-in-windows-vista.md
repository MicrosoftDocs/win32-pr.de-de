---
description: In Windows Vista macht Microsoft Media Foundation Metadaten über die IMF Metadata-Schnittstelle verfügbar.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Metadatenanbieter in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356520"
---
# <a name="metadata-providers-in-windows-vista"></a>Metadatenanbieter in Windows Vista

In Windows Vista macht Microsoft Media Foundation Metadaten über die [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle verfügbar.

## <a name="reading-metadata"></a>Lesen von Metadaten

Um Metadaten aus einer Medienquelle zu lesen, führen Sie die folgenden Schritte aus:

1.  Einen Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle erhalten. Sie können die [**imfsourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstelle verwenden, um einen **imfmediasource** -Zeiger zu erhalten.
2.  Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) zum Abrufen des Präsentations Deskriptors der Medienquelle.
3.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für die Medienquelle, um einen Zeiger auf die [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) -Schnittstelle zu erhalten. Geben Sie im *guidservice* -Parameter von **MF-Service** den Wert **MF \_ - \_ metadatenanbieterdienst \_** an. Wenn die Quelle die **IMFMetadataProvider** -Schnittstelle nicht unterstützt, gibt **MF-Service** einen **\_ \_ nicht \_ unterstützten MF-Dienst** zurück.
4.  Aufrufen von [**IMFMetadataProvider:: getmfmetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) und übergeben eines Zeigers an den Präsentations Deskriptor. Diese Methode gibt einen Zeiger auf die [**imfmetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle zurück.
    -   Zum Abrufen von Metadaten auf Streamebene müssen Sie zuerst [**imfstreamdescriptor:: getstreamidentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) aufrufen, um den Datenstrom Bezeichner zu erhalten. Übergeben Sie dann den Datenstrom Bezeichner im *dwstreamidentifier* -Parameter von [**getmfimetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).
    -   Legen Sie zum Aufrufen von Metadaten auf Präsentationsebene *dwstreamidentifier* auf 0 (null) fest.
5.  \[Optional \] [**: imfmetadata:: getalllanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) aufrufen, um eine Liste der Sprachen zu erhalten, in denen Metadaten verfügbar sind. Sprachen werden mithilfe von RFC 1766-kompatiblen sprach Tags identifiziert.
6.  \[Optionaler \] Rückruf [**imfmetadata:: setLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) , um die Sprache auszuwählen.
7.  \[Optional \] [**: imfmetadata:: getallpropertynames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) aufrufen, um eine Liste der Namen aller Metadateneigenschaften für diesen Stream oder diese Präsentation abzurufen.
8.  Wenn Sie [**imfmetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) aufrufen, um einen bestimmten Wert für die Metadateneigenschaft abzurufen, übergeben Sie den Namen der Eigenschaft.

Der folgende Code zeigt die Schritte 2 – 4:


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



Der folgende Code zeigt die Schritte 7 – 8. Angenommen, `DisplayProperty` Es handelt sich um eine Funktion, die einen **PROPVARIANT** -Wert anzeigt.


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Metadaten](media-metadata.md)
</dt> <dt>

[Shellmetadatenanbieter](shell-metadata-providers.md)
</dt> </dl>

 

 



