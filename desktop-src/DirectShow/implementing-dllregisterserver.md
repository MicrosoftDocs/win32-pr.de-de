---
description: Implementieren von DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementieren von DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39d55b73dd70a21c10df26a100f964917a57dd9f036ebd5c2708359bca1dd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998091"
---
# <a name="implementing-dllregisterserver"></a>Implementieren von DllRegisterServer

Der letzte Schritt besteht darin, die **DllRegisterServer-Funktion** zu implementieren. Die DLL, die die Komponente enthält, muss diese Funktion exportieren. Die Funktion wird von einer eingerichteten Anwendung aufgerufen, oder wenn der Benutzer das Regsvr32.exe Tool ausführt.

Das folgende Beispiel zeigt eine minimale Implementierung von **DlLRegisterServer:**


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



Die [**Funktion AMovieDllRegisterServer2**](amoviedllregisterserver2.md) erstellt Registrierungseinträge für jede Komponente in der


```
g_Templates
```



Array. Diese Funktion weist jedoch einige Einschränkungen auf. Zunächst wird jeder Filter der Kategorie "DirectShow-Filter" (CLSID \_ LegacyAmFilterCategory) zugewiesen, aber nicht jeder Filter gehört zu dieser Kategorie. Erfassungsfilter und Komprimierungsfilter verfügen beispielsweise über eigene Kategorien. Wenn Ihr Filter ein Hardwaregerät unterstützt, müssen Sie möglicherweise zwei zusätzliche Informationen registrieren, die **AMovieDLLRegisterServer2** nicht verarbeitet: das *Medium* und die *Pinkategorie*. Ein Medium definiert eine Kommunikationsmethode in einem Hardwaregerät, z. B. einem Bus. Die Stecknadelkategorie definiert die Funktion eines Stecknadels. Informationen zu Medien finden Sie unter "KSPIN \_ MEDIUM" im Microsoft Windows Driver Development Kit (DDK). Eine Liste der Stecknadelkategorien finden Sie unter [Anheften von Eigenschaftensatz.](pin-property-set.md)

Wenn Sie eine Filterkategorie, ein Medium oder eine Pinkategorie angeben möchten, rufen Sie die [**IFilterMapper2::RegisterFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) in **DllRegisterServer** auf. Diese Methode verwendet einen Zeiger auf eine [**REGFILTER2-Struktur,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) die Informationen zum Filter angibt.

Um dies etwas zu erschweren, unterstützt die **REGFILTER2-Struktur** zwei verschiedene Formate zum Registrieren von Pins. Der **dwVersion-Member** gibt das Format an:

-   Wenn **dwVersion** 1 ist, lautet das Stecknadelformat **AMOVIESETUP \_ PIN** (zuvor beschrieben).
-   Wenn **dwVersion** 2 ist, lautet das Stecknadelformat [**REGFILTERPINS2.**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2)

Die **REGFILTERPINS2-Struktur** enthält Einträge für Pinmedien und Pinkategorien. Außerdem werden Bitflags für einige Elemente verwendet, die **von der AMOVIESETUP-PIN \_** als boolesche Werte deklariert werden.

Im folgenden Beispiel wird gezeigt, wie **IFilterMapper2::RegisterFilter** innerhalb von **DllRegisterServer** aufgerufen wird:


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



