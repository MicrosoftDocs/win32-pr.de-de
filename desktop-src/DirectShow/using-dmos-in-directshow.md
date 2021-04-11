---
description: Verwenden von dmos in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Verwenden von dmos in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131885"
---
# <a name="using-dmos-in-directshow"></a>Verwenden von dmos in DirectShow

Anwendungen, die auf DirectShow basieren, können DMOS in einem Filter Diagramm über den [DMO-Wrapper](dmo-wrapper-filter.md) Filter verwenden. Mit diesem Filter wird ein DMO aggregiert und alle Details der Verwendung des DMO behandelt, z. b. das Übergeben von Daten an und aus dem DMO, das Zuordnen von [**imediabuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) -Objekten usw.

Da der DMO durch den Filter aggregiert wird, kann die Anwendung den Filter nach allen vom DMO verfügbar gemachten com-Schnittstellen Abfragen. Die Anwendung sollte den Filter jedoch alle Streamingvorgänge für den DMO verarbeiten lassen. Legen Sie z. b. keine Medientypen fest, verarbeiten Sie alle Puffer, leeren Sie den DMO, Sperren Sie DMO, aktivieren oder deaktivieren Sie die Qualitätskontrolle, oder legen Sie Video Optimierungen fest.

Wenn Sie die Klassen-ID (CLSID) eines bestimmten DMO kennen, das Sie verwenden möchten, können Sie den DMO-Wrapper Filter mit diesem DMO wie folgt initialisieren:

1.  Rufen Sie **cokreateinstance** auf, um den DMO-Wrapper Filter zu erstellen.
2.  Fragen Sie den DMO-Wrapper Filter für die [**idmowrapperfilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) -Schnittstelle ab.
3.  Nennen Sie die [**idmuwrapperfilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) -Methode. Geben Sie die CLSID des DMO und die GUID der Kategorie des DMO an. Eine Liste der DMO-Kategorien finden Sie unter [DMO-GUIDs](dmo-guids.md).

Diese Schritte sind im folgenden Code dargestellt:


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



Die [**dmuenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion Listet DMOS in der Registrierung auf. Diese Funktion verwendet einen anderen Satz von Kategorien-GUIDs, die für DirectShow-Filter verwendet werden.

**Verwenden des Enumerators für System Geräte mit DMOS**

Anstatt ein DMO direkt zu erstellen, können Sie den [Enumerator für System Geräte](system-device-enumerator.md)verwenden, der jede von der **dmoenum** -Methode unterstützte DMO-Kategorie auflisten kann. Der Enumerator für System Geräte enthält auch DMOS, wenn er bestimmte DirectShow-Filter Kategorien auflistet. Die folgende Tabelle zeigt die Zuordnung zwischen DMO-Kategorien und DirectShow-Kategorien.



|                             |                                |
|-----------------------------|--------------------------------|
| DMO-Kategorie                | DirectShow-Entsprechung          |
| dmucategory \_ - \_ Audioencoder | CLSID \_ audiocompressorcategory |
| dmucategory \_ - \_ Audiodecoder | CLSID \_ legacyamfiltercategory  |
| dmucategory- \_ Video \_ Encoder | CLSID \_ videocompressorcategory |
| dmucategory- \_ Video \_ Decoder | CLSID \_ legacyamfiltercategory  |



 

Der Enumerator für System Geräte gibt eine Liste der monikerobjekte zurück. Wenn der Moniker ein DMO darstellt, erstellt die **IMoniker:: BindTo Object** -Methode automatisch den DMO-Wrapper Filter und initialisiert ihn mit diesem DMO. Folglich ist die Tatsache, dass ein DMO beteiligt ist, für die Anwendung transparent. Weitere Informationen zur Verwendung des Enumerators für Systemgeräte finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).

**Einschränkungen**

Bei der Verwendung von dmos in DirectShow sind einige Einschränkungen zu beachten:

-   Der DMO-Wrapper Filter unterstützt keine DMOS mit NULL Eingaben, mehreren Eingaben oder null Ausgaben.
-   Alle Pin-Verbindungen im DMO-Wrapper Filter verwenden die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle.
-   DirectShow-Bearbeitungs Dienste unterstützen keine DMO-basierten Effekte oder Übergänge.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von dmos](using-dmos.md)
</dt> </dl>

 

 



