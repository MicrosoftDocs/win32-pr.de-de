---
description: Auswählen eines Komprimierungsfilters
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Auswählen eines Komprimierungsfilters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf964aa3647086efe569263e5fb36b4e0db60ebfad73c9d2fe9dcb14f3bcf125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999220"
---
# <a name="choosing-a-compression-filter"></a>Auswählen eines Komprimierungsfilters

Verschiedene Arten von Softwarekomponenten können eine Video- oder Audiokomprimierung durchführen, z. B.:

-   Native DirectShow-Filter
-   VideoKomprimierungs-Manager-Codecs (VCM)
-   ACM-Codecs (Audio Compression Manager)
-   DirectX-Medienobjekte (DMOs)

In DirectShow werden VCM-Codecs vom [AVI-Filter](avi-compressor-filter.md)umschlossen, und ACM-Codecs werden vom [ACM-Wrapperfilter umschlossen.](acm-wrapper-filter.md) DMOs werden vom DMO [Wrapperfilter umschlossen.](dmo-wrapper-filter.md) Der Systemgeräte-Enumerator bietet eine konsistente Möglichkeit zum Aufzählen und Erstellen eines dieser Typen von Typen, ohne sich Gedanken über das zugrunde liegende Modell machen zu müssen.

Weitere Informationen zum Systemgeräte-Enumerator finden Sie unter [Verwenden des Systemgeräte-Enumerators.](using-the-system-device-enumerator.md) Kurz gesagt werden alle DirectShow-Filter nach Kategorie klassifiziert, und jede Kategorie wird durch eine GUID identifiziert. Für Videovideovideos ist die Kategorie-GUID CLSID \_ VideoCompressorCategory. Für Audiowiedergaben ist dies CLSID \_ AudioCompressorCategory. Zum Aufzählen einer bestimmten Kategorie erstellt der Systemgeräte-Enumerator ein *Enumeratorobjekt,* das die [**IEnumMoniker-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) unterstützt. Die Anwendung verwendet diese Schnittstelle, um Gerätemoniker abzurufen, wobei jeder Gerätemoniker eine Instanz eines DirectShow-Filters darstellt. Sie können den Moniker verwenden, um den Filter zu erstellen oder den Angezeigten Namen des Geräts zu erhalten, ohne den Filter zu erstellen.

Gehen Sie wie folgt vor, um die video- oder audio-Audiowiedergaben aufzählen zu können, die auf dem System des Benutzers verfügbar sind:

1.  Rufen [**Sie CoCreateInstance auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) um den Systemgeräte-Enumerator zu erstellen, der über die Klassen-ID CLSID \_ SystemDeviceEnum verfügt.
2.  Rufen [**Sie ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der Filterkategorie-GUID auf. Die -Methode gibt einen **IEnumMoniker-Schnittstellenzeiger** zurück.
3.  Verwenden Sie die IEnumMoniker::Next-Methode, um die Gerätemoniker zu aufzählen. Diese Methode gibt eine [**IMoniker-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-imoniker) zurück, die den Moniker darstellt.

Gehen Sie wie folgt vor, um den Benutzernamen aus einem Moniker zu erhalten:

1.  Rufen Sie **die IMoniker::BindToStorage-Methode** auf. Diese Methode gibt einen **IPropertyBag-Schnittstellenzeiger** zurück.
2.  Verwenden Sie **die IPropertyBag::Read-Methode,** um die **FriendlyName-Eigenschaft zu** lesen.

In der Regel würde eine Anwendung eine Liste von Darstellungen anzeigen, sodass der Benutzer eine auswählen kann. Der folgende Code füllt z. B. ein Listenfeld mit den Namen der verfügbaren Videobeobarungen auf.


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



Um eine Filterinstanz aus dem Moniker zu erstellen, rufen Sie die **IMoniker::BindToObject-Methode** auf. Die -Methode gibt einen [**IBaseFilter-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) zurück.


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



Bei VCM-Codecs stellt jeder Moniker einen bestimmten Codec dar, obwohl alle Codecs vom gleichen AVI-Komprimierungsfilter umschlossen sind. Durch **Aufrufen von BindToObject** wird eine Instanz dieses Filters erstellt, die für diesen Codec initialisiert wird. Aus diesem Grund können Sie **CoCreateInstance** nicht direkt im FILTER DER AVI-Komprimierung aufrufen. Sie müssen den Systemgeräte-Enumerator durchgehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneutes Dekomprimieren einer AVI-Datei](recompressing-an-avi-file.md)
</dt> </dl>

 

 
