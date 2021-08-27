---
description: Verwenden des Systemgeräte-Enumerators
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Verwenden des Systemgeräte-Enumerators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7192a1ea85d807dd388b79eef455edf59c83d3c22ab3a4a330799b3491253bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083534"
---
# <a name="using-the-system-device-enumerator"></a>Verwenden des Systemgeräte-Enumerators

Der Systemgeräte-Enumerator bietet eine einheitliche Möglichkeit, die auf dem System eines Benutzers registrierten Filter nach Kategorie zu aufzählen. Darüber hinaus wird zwischen einzelnen Hardwaregeräten unterschieden, auch wenn sie vom gleichen Filter unterstützt werden. Dies ist besonders nützlich für Geräte, die das Windows Driver Model (WDM) und den KSProxy-Filter verwenden. Beispielsweise kann der Benutzer über mehrere WDM-Videoaufnahmegeräte verfügen, die alle vom gleichen Filter unterstützt werden. Der Systemgeräte-Enumerator behandelt sie als separate Geräteinstanzen.

Der Systemgeräte-Enumerator erstellt einen Enumerator für eine bestimmte Kategorie, z. B. Audioaufnahme oder Videokomprimierung. Der Kategorie-Enumerator gibt einen eindeutigen Moniker für jedes Gerät in der Kategorie zurück. Der Kategorie-Enumerator enthält automatisch alle relevanten Plug & Play geräte in der Kategorie. Eine Liste der Kategorien finden Sie unter [FilterKategorien](filter-categories.md).

Gehen Sie wie folgt vor, um den Systemgeräte-Enumerator zu verwenden:

1.  Erstellen Sie den Systemgeräte-Enumerator, indem Sie **CoCreateInstance aufrufen.** Der Klassenbezeichner (CLSID) ist CLSID \_ SystemDeviceEnum.
2.  Rufen Sie einen Kategorieenumerator ab, indem Sie [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der CLSID der gewünschten Kategorie aufrufen. Diese Methode gibt einen **IEnumMoniker-Schnittstellenzeiger** zurück. Wenn die Kategorie leer ist (oder nicht vorhanden ist), gibt die Methode anstelle eines Fehlercodes S \_ FALSE zurück. Wenn dies der Wert ist, ist der **zurückgegebene IEnumMoniker-Zeiger** **NULL,** und eine Deferencierung verursacht eine Ausnahme. Testen Sie daher explizit auf S OK, wenn Sie \_ **CreateClassEnumerator** aufrufen, anstatt das übliche **SUCCEEDED-Makro auf** aufruft.
3.  Verwenden Sie **die IEnumMoniker::Next-Methode,** um jeden Moniker zu aufzählen. Diese Methode gibt einen **IMoniker-Schnittstellenzeiger** zurück. Wenn die **Next-Methode** das Ende der Enumeration erreicht, gibt sie auch S FALSE zurück. Überprüfen Sie daher erneut \_ auf S \_ OK.
4.  Um den Anzeigenamen des Geräts abzurufen (z. B. zur Anzeige auf der Benutzeroberfläche), rufen Sie die **IMoniker::BindToStorage-Methode** auf.
5.  Um den DirectShow-Filter zu erstellen und zu initialisieren, der das Gerät verwaltet, rufen Sie **IMoniker::BindToObject für** den Moniker auf. Rufen [**Sie IFilterGraph::AddFilter auf,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) um dem Diagramm den Filter hinzuzufügen.

Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Aufzählen von Geräten](images/sysdevenum.png)

Im folgenden Beispiel wird gezeigt, wie Sie die video-Videos aufzählen, die auf dem System des Benutzers installiert sind. Zur Besserung führt das Beispiel eine minimale Fehlerüberprüfung aus.


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



**Gerätemoniker**

Für Gerätemoniker können Sie den Moniker an die [**IFilterGraph2::AddSourceFilterForMoniker-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) übergeben, um einen Erfassungsfilter für das Gerät zu erstellen. Beispielcode finden Sie in der Dokumentation für diese Methode.

Die **IMoniker::GetDisplayName-Methode** gibt den Anzeigenamen des Monikers zurück. Obwohl der Anzeigename lesbar ist, wird er in der Regel nicht für Endbenutzer angezeigt. Sie können stattdessen den Benutzerfreundlichen Namen aus der Eigenschaftentüte erhalten, wie zuvor beschrieben.

Mit **der IMoniker::P arseDisplayName-Methode** oder der **MkParseDisplayName-Funktion** kann ein Standardgerätemoniker für eine bestimmte Filterkategorie erstellt werden. Verwenden Sie einen Anzeigenamen im Formular `@device:*:{category-clsid}` , wobei `category-clsid` die Zeichenfolgendarstellung der Kategorie-GUID ist. Der Standardmoniker ist der erste Moniker, der vom Geräteenumerator für diese Kategorie zurückgegeben wird.

 

 



