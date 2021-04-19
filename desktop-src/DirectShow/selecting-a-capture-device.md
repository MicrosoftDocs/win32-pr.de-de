---
description: Auswählen eines Erfassungs Geräts
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Auswählen eines Erfassungs Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342725"
---
# <a name="selecting-a-capture-device"></a>Auswählen eines Erfassungs Geräts

Verwenden Sie zum Auswählen eines Audiogeräts oder Video Erfassungs Geräts den [Enumerator "Systemgeräte](system-device-enumerator.md)", der im Thema [Verwenden des Enumerators "Systemgeräte](using-the-system-device-enumerator.md)" beschrieben wird. Der Enumerator für System Geräte gibt eine Sammlung von gerätermonikern zurück, die nach Gerätekategorie ausgewählt ist. Ein *Moniker* ist ein COM-Objekt, das Informationen über ein anderes Objekt enthält. Moniker ermöglichen es der Anwendung, Informationen zu einem Objekt zu erhalten, ohne das Objekt tatsächlich zu erstellen. Später kann die Anwendung den Moniker zum Erstellen des Objekts verwenden. Weitere Informationen zu Monikern finden Sie in der Dokumentation für [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Führen Sie die folgenden Schritte aus, um den Enumerator für System Geräte zu verwenden.

1.  Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine Instanz des Enumerators für System Geräte zu erstellen.
2.  Nennen Sie [**ikreatedevenum:: feateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) , und geben Sie die Gerätekategorie als GUID an. Für Erfassungsgeräte sind die folgenden Kategorien relevant. 

    | Kategorie-GUID                       | BESCHREIBUNG           |
    |-------------------------------------|-----------------------|
    | **CLSID \_ audioinputentvicecategory** | Audioerfassungs Geräte |
    | **CLSID \_ videoinputentvicecategory** | Video Erfassungsgeräte |

    

     

    Wenn eine Videokamera über ein integriertes Mikrofon verfügt, wird Sie in beiden Kategorien angezeigt. Die Kamera und das Mikrofon werden jedoch vom System als separate Geräte behandelt, um Aufzählungs-, Geräte-und datenstreamingvorgänge durchlaufen zu können.

3.  Die Methode " [**kreateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) " gibt einen Zeiger auf die [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) -Schnittstelle zurück. Um die Moniker aufzuzählen, nennen Sie [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

Mit dem folgenden Code wird ein Enumerator für eine angegebene Gerätekategorie erstellt.


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



Mit der [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) -Schnittstelle wird eine Liste der [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstellen aufgelistet, von denen jede einen gerätermoniker darstellt. Die Anwendung kann Eigenschaften aus dem Moniker lesen oder den Moniker zum Erstellen eines DirectShow-Erfassungs Filters für das Gerät verwenden. Monikereigenschaften werden als **Variant** -Werte zurückgegeben. Die folgenden Eigenschaften werden von gerätermonikern unterstützt.



| Eigenschaft       | BESCHREIBUNG                                                               | VARIANT-Typ |
|----------------|---------------------------------------------------------------------------|--------------|
| FriendlyName | Der Name des Geräts.                                                   | **VT \_ BSTR** |
| Beschreibung  | Eine Beschreibung des Geräts.                                              | **VT \_ BSTR** |
| DevicePath   | Eine eindeutige Zeichenfolge, die das Gerät identifiziert. (Nur Video Erfassungsgeräte.) | **VT \_ BSTR** |
| "Waveingeid"     | Der Bezeichner für ein audioerfassungs Gerät. (Nur audioerfassungs Geräte.) | **VT \_ I4**   |



 

Die Eigenschaften "FriendlyName" und "Description" sind für die Anzeige in einer Benutzeroberfläche geeignet.

-   Die Eigenschaft "FriendlyName" ist für jedes Gerät verfügbar. Sie enthält einen lesbaren Namen für das Gerät.
-   Die "Description"-Eigenschaft ist nur für DV-und D-VHS/MPEG-Camcorder-Geräte verfügbar. Weitere Informationen finden Sie unter [msdv Driver](msdv-driver.md) und [mstape Driver](mstape-driver.md). Wenn Sie verfügbar ist, enthält Sie eine Beschreibung des Geräts, das spezifischer ist als die Eigenschaft "FriendlyName". In der Regel enthält Sie den Herstellernamen.
-   Die Eigenschaft "DevicePath" ist keine für menschenlesbare Zeichenfolge, Sie ist jedoch für jedes Video Erfassungsgerät im System eindeutig. Mit dieser Eigenschaft können Sie zwischen zwei oder mehr Instanzen desselben Geräte Modells unterscheiden.
-   Wenn die Eigenschaft "waveinid" vorhanden ist, bedeutet dies, dass der DirectShow-Erfassungs Filter die [Waveform-audioapis](../multimedia/waveform-audio.md) intern verwendet, um mit dem Gerät zu kommunizieren. Der Wert der waveiniid-Eigenschaft entspricht dem Bezeichner, der von den **\* WaveIn* _-Funktionen verwendet wird, z. b. [_ *waveiniopen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Führen Sie die folgenden Schritte aus, um Eigenschaften aus dem Moniker zu lesen.

1.  Aufrufen von [**IMoniker:: bindesstorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) zum Abrufen eines Zeigers auf die [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) -Schnittstelle.
2.  Aufrufen von **IPropertyBag:: Read** , um die Eigenschaft zu lesen.

Im folgenden Codebeispiel wird gezeigt, wie Sie eine Liste von gerätermonikern auflisten und die Eigenschaften erhalten.


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



Um einen DirectShow-Erfassungs Filter für das Gerät zu erstellen, rufen Sie die [**IMoniker:: BindTo Object**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) -Methode auf, um einen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger abzurufen. Klicken Sie dann auf [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , um dem Filter Diagramm den Filter hinzuzufügen:


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

[Audioerfassung](audio-capture.md)
</dt> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 
