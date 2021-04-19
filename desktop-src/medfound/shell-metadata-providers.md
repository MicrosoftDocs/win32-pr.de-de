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
# <a name="shell-metadata-providers"></a>Shellmetadatenanbieter

Ab Windows 7 macht Microsoft Media Foundation Metadaten über die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle verfügbar.

Metadaten, die mit dem in diesem Thema definierten Prozess abgerufen werden, sollten nur für den schreibgeschützten Zugriff verwendet werden. Das Schreiben von Daten mit diesem Prozess wird nicht unterstützt. Sie können ein [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekt zu Schreib Zwecken mithilfe eines Klassen Bezeichners (CLSID) erstellen, der von [**pslookuppropertyhandlerclsid**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid)abgerufen wurde.

## <a name="reading-metadata"></a>Lesen von Metadaten

Um Metadaten aus einer Medienquelle zu lesen, führen Sie die folgenden Schritte aus:

1.  Einen Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle erhalten. Sie können die [**imfsourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstelle verwenden, um einen **imfmediasource** -Zeiger zu erhalten.
2.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für die Medienquelle, um einen Zeiger auf die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle zu erhalten. Geben Sie im *guidservice* -Parameter von **MF-Service** den Wert **MF- \_ eigenschaftenhandlerdienst \_ \_** an. Wenn die Quelle die **IPropertyStore** -Schnittstelle nicht unterstützt, gibt **MF-Service** einen **\_ \_ nicht \_ unterstützten MF-Dienst** zurück.
3.  Aufrufen von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Methoden zum Aufzählen der Metadateneigenschaften.

Der folgende Code zeigt diese Schritte. Angenommen, `DisplayProperty` Es handelt sich um eine Funktion, die einen **PROPVARIANT** -Wert anzeigt.


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



Eine Liste der Metadaten-Eigenschafts Schlüssel finden Sie unter [Metadateneigenschaften für Mediendateien](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Metadaten](media-metadata.md)
</dt> </dl>

 

 
