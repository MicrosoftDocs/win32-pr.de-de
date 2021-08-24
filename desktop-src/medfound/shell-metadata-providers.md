---
description: Ab Windows 7 macht Microsoft Media Foundation Metadaten über die IPropertyStore-Schnittstelle verfügbar.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Shellmetadatenanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31960ed41743a86b62b63555236d2876166a14b098f0692f3d6cb22b051e338e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713360"
---
# <a name="shell-metadata-providers"></a>Shellmetadatenanbieter

Ab Windows 7 macht Microsoft Media Foundation Metadaten über die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) verfügbar.

Metadaten, die mithilfe des in diesem Thema definierten Prozesses abgerufen werden, sollten nur für den schreibgeschützten Zugriff verwendet werden. Das Schreiben von Daten mit diesem Prozess wird nicht unterstützt. Sie können ein [**IPropertyStore-Objekt**](/windows/win32/api/propsys/nn-propsys-ipropertystore) zu Schreibzwecken erstellen, indem Sie einen Klassenbezeichner (CLSID) verwenden, der aus [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid)abgerufen wird.

## <a name="reading-metadata"></a>Lesen von Metadaten

Führen Sie die folgenden Schritte aus, um Metadaten aus einer Medienquelle zu lesen:

1.  Abrufen eines Zeigers auf die [**INTERFACESMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) der Medienquelle. Sie können die [**INTERFACESSourceResolver-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) verwenden, um einen **POINTERMediaSource-Zeiger** abzurufen.
2.  Rufen Sie [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für die Medienquelle auf, um einen Zeiger auf die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abzurufen. Geben Sie im *guidService-Parameter* von **MFGetService** den Wert **MF PROPERTY HANDLER \_ \_ \_ SERVICE** an. Wenn die Quelle die **IPropertyStore-Schnittstelle** nicht unterstützt, gibt **MFGetService** **MF E \_ \_ UNSUPPORTED \_ SERVICE** zurück.
3.  Rufen Sie [**IPropertyStore-Methoden**](/windows/win32/api/propsys/nn-propsys-ipropertystore) auf, um die Metadateneigenschaften aufzuzählen.

Der folgende Code zeigt diese Schritte. Angenommen, es handelt sich `DisplayProperty` um eine Funktion, die einen **PROPVARIANT-Wert** anzeigt.


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



Eine Liste der Metadateneigenschaftsschlüssel finden Sie unter [Metadateneigenschaften für Mediendateien.](metadata-properties-for-media-files.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienmetadaten](media-metadata.md)
</dt> </dl>

 

 
