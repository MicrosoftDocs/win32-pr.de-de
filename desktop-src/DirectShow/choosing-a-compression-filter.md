---
description: Auswählen eines Komprimierungs Filters
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Auswählen eines Komprimierungs Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125510"
---
# <a name="choosing-a-compression-filter"></a>Auswählen eines Komprimierungs Filters

Verschiedene Arten von Softwarekomponenten können Video-oder Audiokomprimierung durchführen, z. b.:

-   Native DirectShow-Filter
-   Codecs für Video Komprimierungs-Manager (VCM)
-   Codecs für den Audiokomprimierungs-Manager (ACM)
-   DirectX Media Objects (DMOs)

In DirectShow werden VCM-Codecs durch den [AVI-Kompressor-Filter](avi-compressor-filter.md)umschlossen, und ACM-Codecs werden durch den [ACM-Wrapper Filter](acm-wrapper-filter.md)umschlossen. DMOS werden durch den [DMO-Wrapper Filter](dmo-wrapper-filter.md)umschlossen. Der Enumerator für Systemgeräte bietet eine konsistente Möglichkeit zum Auflisten und Erstellen eines dieser kompressortypen, ohne sich Gedanken über das zugrunde liegende Modell machen zu müssen.

Ausführliche Informationen zum Enumerator für Systemgeräte finden [Sie unter Verwenden des Systemgeräte Enumerators](using-the-system-device-enumerator.md). Kurz gesagt, alle DirectShow-Filter werden nach Kategorie klassifiziert, und jede Kategorie wird durch eine GUID identifiziert. Bei Video-Kompressoren lautet die Kategorie GUID CLSID \_ videocompressorcategory. Für audiokompressoren ist es CLSID \_ audiocompressorcategory. Zum Auflisten einer bestimmten Kategorie erstellt der Systemgeräte Enumerator ein *Enumeratorobjekt* , das die [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) -Schnittstelle unterstützt. Diese Schnittstelle wird von der Anwendung zum Abrufen von gerätermonikern verwendet, wobei jeder gerätermoniker eine Instanz eines DirectShow-Filters darstellt. Sie können den Moniker verwenden, um den Filter zu erstellen, oder um den anzeigen amen des Geräts zu erhalten, ohne den Filter zu erstellen.

Gehen Sie folgendermaßen vor, um die auf dem System des Benutzers verfügbaren Video-oder audiokompressoren aufzulisten:

1.  Rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Enumerator für Systemgeräte zu erstellen, der über die Klassen-ID CLSID \_ systemdeviceenumeration verfügt.
2.  Aufrufen von [**ikreatedevenum:: kreateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der Filterkategorie GUID. Die-Methode gibt einen **IEnumMoniker** -Schnittstellen Zeiger zurück.
3.  Verwenden Sie die IEnumMoniker:: Next-Methode, um die gerätermoniker aufzuzählen. Diese Methode gibt eine [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) -Schnittstelle zurück, die den Moniker darstellt.

Gehen Sie folgendermaßen vor, um den anzeigen Amen von einem Moniker zu erhalten:

1.  Aufrufen der **IMoniker:: bindesstorage** -Methode. Diese Methode gibt einen **IPropertyBag** -Schnittstellen Zeiger zurück.
2.  Verwenden Sie die **IPropertyBag:: Read** -Methode, um die **FriendlyName** -Eigenschaft zu lesen.

In der Regel würde eine Anwendung eine Liste von Kompressoren anzeigen, sodass der Benutzer eine Liste auswählen kann. Der folgende Code füllt z. b. ein Listenfeld mit den Namen der verfügbaren Video-Kompressoren auf.


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



Um eine Filter Instanz aus dem Moniker zu erstellen, rufen Sie die **IMoniker:: BindTo Object** -Methode auf. Die-Methode gibt einen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger zurück.


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



Bei VCM-Codecs stellt jeder Moniker einen bestimmten Codec dar, auch wenn alle Codecs durch denselben AVI-Komprimierungs Filter umschließt werden. Der Aufruf von " **BindToObject** " erstellt eine Instanz dieses Filters, die für diesen Codec initialisiert wird. Aus diesem Grund können Sie **cokreateinstance** nicht direkt für den AVI-Komprimierungs Filter aufrufen. Sie müssen den Enumerator "Systemgeräte" durchlaufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neukomprimieren einer AVI-Datei](recompressing-an-avi-file.md)
</dt> </dl>

 

 
