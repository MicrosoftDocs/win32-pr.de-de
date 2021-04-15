---
description: Verwenden des Enumerators für System Geräte
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Verwenden des Enumerators für System Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556421"
---
# <a name="using-the-system-device-enumerator"></a>Verwenden des Enumerators für System Geräte

Der Enumerator für System Geräte bietet eine einheitliche Möglichkeit zum Auflisten der auf dem System eines Benutzers registrierten Filter, nach Kategorie. Außerdem unterscheidet es sich zwischen einzelnen Hardware Geräten, auch wenn Sie vom gleichen Filter unterstützt werden. Dies ist besonders nützlich für Geräte, die die Windows-Treibermodell (WDM) und den ksproxy-Filter verwenden. Der Benutzer kann z. b. über mehrere WDM-Video Erfassungsgeräte verfügen, die alle vom gleichen Filter unterstützt werden. Der Enumerator für System Geräte behandelt diese als separate Geräte Instanzen.

Der Enumerator für System Geräte erstellt einen Enumerator für eine bestimmte Kategorie, z. b. Audioerfassung oder Video Komprimierung. Der kategorieenumerator gibt einen eindeutigen Moniker für jedes Gerät in der Kategorie zurück. Der kategorieenumerator enthält automatisch alle relevanten Plug & Play Geräte in der Kategorie. Eine Liste der Kategorien finden Sie unter [Filter Kategorien](filter-categories.md).

Gehen Sie folgendermaßen vor, um den Enumerator für System Geräte zu verwenden:

1.  Erstellen Sie den Enumerator für Systemgeräte durch Aufrufen von **CoCreateInstance**. Der Klassen Bezeichner (CLSID) ist CLSID \_ systemdeviceenum.
2.  Abrufen eines kategorieenumerators durch Aufrufen von [**icreatedevenum:: createclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der CLSID der gewünschten Kategorie. Diese Methode gibt einen **IEnumMoniker** -Schnittstellen Zeiger zurück. Wenn die Kategorie leer ist (oder nicht vorhanden ist), gibt die Methode " \_ false" anstelle eines Fehlercodes zurück. Wenn dies der Fall ist, ist der zurückgegebene **IEnumMoniker** -Zeiger **null** , und Dereferenzierung führt zu einer Ausnahme. Testen Sie daher explizit auf " \_ OK", wenn Sie " **createclassenumschlag**" aufrufen, statt das übliche Makro " **erfolgreich** " aufzurufen.
3.  Verwenden Sie die **IEnumMoniker:: Next** -Methode, um jeden Moniker aufzuzählen. Diese Methode gibt einen **IMoniker** -Schnittstellen Zeiger zurück. Wenn die **nächste** Methode das Ende der Enumeration erreicht, gibt Sie auch s \_ false zurück. Überprüfen Sie daher erneut auf \_ OK.
4.  Rufen Sie zum Abrufen des anzeigen Amens des Geräts (z. b. zur Anzeige auf der Benutzeroberfläche) die **IMoniker:: bindesstorage** -Methode auf.
5.  Um den DirectShow-Filter zu erstellen und zu initialisieren, der das Gerät verwaltet, rufen Sie **IMoniker:: bindjeobject** für den Moniker auf. Nennen Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , um dem Diagramm den Filter hinzuzufügen.

Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Auflisten von Geräten](images/sysdevenum.png)

Im folgenden Beispiel wird gezeigt, wie die auf dem System des Benutzers installierten Video-Kompressoren aufgelistet werden. Aus Gründen der Übersichtlichkeit führt das Beispiel eine minimale Fehlerüberprüfung durch.


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



**Gerätermoniker**

Für gerätermoniker können Sie den Moniker an die [**IFilterGraph2:: addsourcefilterformoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) -Methode übergeben, um einen Erfassungs Filter für das Gerät zu erstellen. Beispielcode finden Sie in der Dokumentation für diese Methode.

Die **IMoniker:: GetDisplayName** -Methode gibt den anzeigen Amen für den Moniker zurück. Obwohl der Anzeige Name lesbar ist, wird er in der Regel keinem Endbenutzer angezeigt. Verwenden Sie stattdessen den anzeigen Amen aus dem Eigenschaften Behälter, wie zuvor beschrieben.

Mit der **IMoniker::P artardisplayname** -Methode oder der **mkparser-DisplayName** -Funktion kann ein standardgerätermoniker für eine bestimmte Filterkategorie erstellt werden. Verwenden Sie einen anzeigen Amen mit dem Formular `@device:*:{category-clsid}` , wobei `category-clsid` die Zeichen folgen Darstellung der Kategorie-GUID ist. Der standardmoniker ist der erste Moniker, der vom Geräte Enumerator für diese Kategorie zurückgegeben wurde.

 

 



