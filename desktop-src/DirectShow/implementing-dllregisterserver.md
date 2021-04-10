---
description: Implementieren von DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementieren von DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125036"
---
# <a name="implementing-dllregisterserver"></a>Implementieren von DllRegisterServer

Der letzte Schritt besteht darin, die **DllRegisterServer** -Funktion zu implementieren. Die dll, die die Komponente enthält, muss diese Funktion exportieren. Die Funktion wird von einer Setup Anwendung aufgerufen, oder wenn der Benutzer das Regsvr32.exe Tool ausführt.

Das folgende Beispiel zeigt eine minimale Implementierung von **DllRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



Die [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion erstellt Registrierungseinträge für jede Komponente im


```
g_Templates
```



Array. Diese Funktion weist jedoch einige Einschränkungen auf. Zuerst wird jeder Filter der Kategorie "DirectShow Filters" (CLSID \_ legacyamfiltercategory) zugewiesen, aber nicht jeder Filter gehört zu dieser Kategorie. Erfassungs Filter und Komprimierungs Filter verfügen z. b. über eigene Kategorien. Zweitens: Wenn Ihr Filter ein Hardware Gerät unterstützt, müssen Sie möglicherweise zwei weitere Informationen registrieren, die **AMovieDLLRegisterServer2** nicht behandelt: die Kategorie *Mittel* und *Pin*. Ein Medium definiert eine Kommunikationsmethode in einem Hardware Gerät, z. b. einem Bus. Die PIN-Kategorie definiert die Funktion einer PIN. Informationen zu Medien finden Sie unter "kspin- \_ Medium" im Microsoft Windows Driver Development Kit (DDK). Eine Liste der PIN-Kategorien finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md).

Wenn Sie eine Filterkategorie, eine mittlere oder eine PIN-Kategorie angeben möchten, müssen Sie die [**IFilterMapper2:: registerfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) -Methode innerhalb von **DllRegisterServer** aufrufen. Diese Methode nimmt einen Zeiger auf eine [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) -Struktur, die Informationen über den Filter angibt.

Um die Dinge etwas komplizierter zu machen, unterstützt die **REGFILTER2** -Struktur zwei verschiedene Formate zum Registrieren von Pins. Der **dwVersion** -Member gibt das Format an:

-   Wenn **dwVersion** den Wert 1 hat, ist das PIN-Format die **amoviesetup- \_ Pin** (zuvor beschrieben).
-   Wenn **dwVersion** 2 ist, ist das PIN-Format [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).

Die **REGFILTERPINS2** -Struktur enthält Einträge für PIN-Medien und PIN-Kategorien. Außerdem werden Bitflags für einige Elemente verwendet, die von der **amoviesetup- \_ Pin** als boolesche Werte deklariert werden.

Im folgenden Beispiel wird gezeigt, wie **IFilterMapper2:: registerfilter** von innerhalb von **DllRegisterServer** aufgerufen wird:


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



 

 



