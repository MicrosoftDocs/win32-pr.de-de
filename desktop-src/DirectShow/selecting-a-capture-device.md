---
description: Auswählen eines Erfassungsgeräts
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Auswählen eines Erfassungsgeräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bf92692070c8a0191a91559481d5446bf3d4d894c8e7f6aafc2ed9e73a6667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904410"
---
# <a name="selecting-a-capture-device"></a>Auswählen eines Erfassungsgeräts

Verwenden Sie zum Auswählen eines Audio- oder Videoaufnahmegeräts den [Systemgeräte-Enumerator,](system-device-enumerator.md)der im Thema Verwenden des [Systemgeräte-Enumerators beschrieben wird.](using-the-system-device-enumerator.md) Der Systemgeräte-Enumerator gibt eine Sammlung von Gerätemonikern zurück, die nach Gerätekategorie ausgewählt wurden. Ein *Moniker ist* ein COM-Objekt, das Informationen zu einem anderen Objekt enthält. Moniker ermöglichen es der Anwendung, Informationen zu einem Objekt zu erhalten, ohne das Objekt tatsächlich zu erstellen. Später kann die Anwendung den Moniker verwenden, um das Objekt zu erstellen. Weitere Informationen zu Monikern finden Sie in der Dokumentation für [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Führen Sie die folgenden Schritte aus, um den Systemgeräte-Enumerator zu verwenden.

1.  Rufen [**Sie CoCreateInstance auf,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um eine Instanz des Systemgeräte-Enumerators zu erstellen.
2.  Rufen [**Sie ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) auf, und geben Sie die Gerätekategorie als GUID an. Für Erfassungsgeräte sind die folgenden Kategorien relevant. 

    | Kategorie-GUID                       | BESCHREIBUNG           |
    |-------------------------------------|-----------------------|
    | **CLSID \_ AudioInputDeviceCategory** | Audioaufnahmegeräte |
    | **CLSID \_ VideoInputDeviceCategory** | Videoaufnahmegeräte |

    

     

    Wenn eine Videokamera über ein integriertes Mikrofon verfügt, wird sie in beiden Kategorien angezeigt. Die Kamera und das Mikrofon werden jedoch vom System zur Aufzählung, Geräteerstellung und Datenstreaming als separate Geräte behandelt.

3.  Die [**CreateClassEnumerator-Methode**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) gibt einen Zeiger auf die [**IEnumMoniker-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ienummoniker) zurück. Rufen Sie zum Aufzählen der Moniker [**IEnumMoniker::Next auf.**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next)

Der folgende Code erstellt einen Enumerator für eine angegebene Gerätekategorie.


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



Die [**IEnumMoniker-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ienummoniker) listet [**IMoniker-Schnittstellen**](/windows/win32/api/objidl/nn-objidl-imoniker) auf, von denen jede einen Gerätemoniker darstellt. Die Anwendung kann Eigenschaften aus dem Moniker lesen oder den Moniker verwenden, um einen DirectShow-Erfassungsfilter für das Gerät zu erstellen. Monikereigenschaften werden als **VARIANT-Werte** zurückgegeben. Die folgenden Eigenschaften werden von Gerätemonikern unterstützt.



| Eigenschaft       | BESCHREIBUNG                                                               | VARIANT-Typ |
|----------------|---------------------------------------------------------------------------|--------------|
| "FriendlyName" | Der Name des Geräts.                                                   | **VT \_ BSTR** |
| "Beschreibung"  | Eine Beschreibung des Geräts.                                              | **VT \_ BSTR** |
| "DevicePath"   | Eine eindeutige Zeichenfolge, die das Gerät identifiziert. (Nur Videoaufnahmegeräte.) | **VT \_ BSTR** |
| "WaveInID"     | Der Bezeichner für ein Audioaufnahmegerät. (Nur Audioaufnahmegeräte.) | **VT \_ I4**   |



 

Die Eigenschaften "FriendlyName" und "Description" eignen sich für die Anzeige auf einer Benutzeroberfläche.

-   Die Eigenschaft "FriendlyName" ist für jedes Gerät verfügbar. Sie enthält einen lesbaren Namen für das Gerät.
-   Die Eigenschaft "Beschreibung" ist nur für DV- und D-VHS-/MPEG-Geräte verfügbar. Weitere Informationen finden Sie unter [MSDV-Treiber](msdv-driver.md) und [MSTape-Treiber.](mstape-driver.md) Falls verfügbar, enthält sie eine Beschreibung des Geräts, die spezifischer als die Eigenschaft "FriendlyName" ist. In der Regel enthält sie den Herstellernamen.
-   Die Eigenschaft "DevicePath" ist keine für Menschen lesbare Zeichenfolge, sondern garantiert eindeutig für jedes Videoaufnahmegerät im System. Sie können diese Eigenschaft verwenden, um zwischen zwei oder mehr Instanzen desselben Gerätemodells zu unterscheiden.
-   Wenn die Eigenschaft "WaveInID" vorhanden ist, bedeutet dies, dass der DirectShow-Erfassungsfilter die [Waveform-Audio-APIs](../multimedia/waveform-audio.md) intern für die Kommunikation mit dem Gerät verwendet. Der Wert der Eigenschaft "WaveInID" entspricht dem Bezeichner, der von den **\* waveIn* _-Funktionen verwendet wird, z. B. [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Führen Sie die folgenden Schritte aus, um Eigenschaften aus dem Moniker zu lesen.

1.  Rufen [**Sie IMoniker::BindToStorage auf,**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) um einen Zeiger auf die [**IPropertyBag-Schnittstelle**](../com/ipropertybag-and-ipersistpropertybag.md) zu erhalten.
2.  Rufen **Sie IPropertyBag::Read auf,** um die Eigenschaft zu lesen.

Das folgende Codebeispiel zeigt, wie Sie eine Liste von Gerätemonikern auflisten und die Eigenschaften erhalten.


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



Um einen DirectShow-Erfassungsfilter für das Gerät zu erstellen, rufen Sie die [**IMoniker::BindToObject-Methode**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) auf, um einen [**IBaseFilter-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) zu erhalten. Rufen Sie dann [**IFilterGraph::AddFilter auf,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) um dem Filterdiagramm den Filter hinzuzufügen:


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioaufnahme](audio-capture.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 
