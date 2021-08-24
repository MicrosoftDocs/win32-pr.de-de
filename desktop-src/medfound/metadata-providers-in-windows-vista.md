---
description: In Windows Vista macht Microsoft Media Foundation Metadaten über die BERMetadata-Schnittstelle verfügbar.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Metadatenanbieter in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1edf65b59e0f47e603b057f49a76d8721b8733849937cb29fd0afbe0b9b44920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827070"
---
# <a name="metadata-providers-in-windows-vista"></a>Metadatenanbieter in Windows Vista

In Windows Vista macht Microsoft Media Foundation Metadaten über die [**BEFMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) verfügbar.

## <a name="reading-metadata"></a>Lesen von Metadaten

Führen Sie die folgenden Schritte aus, um Metadaten aus einer Medienquelle zu lesen:

1.  Hier erhalten Sie einen Zeiger auf die [**BENUTZEROBERFLÄCHEMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) der Medienquelle. Sie können die [**BENUTZEROBERFLÄCHESourceResolver-Schnittstelle verwenden,**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) um einen **NSMEDIASource-Zeiger** zu erhalten.
2.  Rufen [**Sie DIE MEDIENQUELLE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf, um den Präsentationsdeskriptor der Medienquelle zu erhalten.
3.  Rufen [**Sie MFGetService für**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) die Medienquelle auf, um einen Zeiger auf die [**BENUTZEROBERFLÄCHEMetadataProvider-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) zu erhalten. Geben Sie *im guidService-Parameter* **von MFGetService** den Wert **MF METADATA PROVIDER SERVICE \_ \_ \_ an.** Wenn die Quelle die **BENUTZEROBERFLÄCHEMetadataProvider-Schnittstelle nicht** unterstützt, gibt **MFGetService** **MF E \_ \_ UNSUPPORTED \_ SERVICE zurück.**
4.  Rufen [**Sie DIEMETADATAProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) auf, und übergeben Sie einen Zeiger auf den Präsentationsdeskriptor. Diese Methode gibt einen Zeiger auf die [**BENUTZEROBERFLÄCHEMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) zurück.
    -   Um Metadaten auf Streamebene zu erhalten, rufen [**Sie zuerst DEN STREAMDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) auf, um den Streambezeichner zu erhalten. Übergeben Sie dann den Streambezeichner im *dwStreamIdentifier-Parameter* von [**GetMFMetadata.**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata)
    -   Legen Sie *dwStreamIdentifier* auf 0 (null) fest, um Metadaten auf Präsentationsebene zu erhalten.
5.  \[Rufen \] Sie optional DEN Aufruf VON [**VORMMETADATA::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) auf, um eine Liste der Sprachen zu erhalten, in denen Metadaten verfügbar sind. Sprachen werden mit RFC 1766-kompatiblen Sprachtags identifiziert.
6.  \[Optional rufen Sie ZUM Auswählen der Sprache DEN Aufruf \] [**VON VORNMETADATA::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) auf.
7.  \[Rufen \] Sie optional DEN NAMEN DER METADATEN [**AUF::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) auf, um eine Liste der Namen aller Metadateneigenschaften für diesen Stream oder diese Präsentation zu erhalten.
8.  Rufen [**Sie DURCHMETADATA::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) auf, um einen bestimmten Metadateneigenschaftswert zu erhalten, und übergeben Sie dabei den Namen der Eigenschaft.

Der folgende Code zeigt die Schritte 2 bis 4:


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



Der folgende Code zeigt die Schritte 7 bis 8. Angenommen, `DisplayProperty` es handelt sich um eine Funktion, die einen **PROPVARIANT-Wert** anzeigt.


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

[Medienmetadaten](media-metadata.md)
</dt> <dt>

[Shellmetadatenanbieter](shell-metadata-providers.md)
</dt> </dl>

 

 



