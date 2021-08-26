---
description: Verwenden von DMOs in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Verwenden von DMOs in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078650"
---
# <a name="using-dmos-in-directshow"></a>Verwenden von DMOs in DirectShow

Anwendungen, die auf DirectShow basieren, können DMOs in einem Filterdiagramm über den DMO [Wrapperfilter](dmo-wrapper-filter.md) verwenden. Dieser Filter aggregiert eine DMO und verarbeitet alle Details der Verwendung von DMO, z. B. das Übergeben von Daten an und aus der DMO, das Zuordnen von [**IMediaBuffer-Objekten**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) usw.

Da die DMO durch den Filter aggregiert wird, kann die Anwendung den Filter nach allen COM-Schnittstellen abfragen, die der DMO verfügbar macht. Die Anwendung sollte es dem Filter jedoch gestatten, alle Streamingvorgänge auf dem DMO. Legen Sie z. B. keine Medientypen fest, verarbeiten Sie puffer, leeren Sie die DMO, sperren Sie die DMO, aktivieren oder deaktivieren Sie die Qualitätssteuerung, oder legen Sie Videooptimierungen fest.

Wenn Sie den Klassenbezeichner (CLSID) eines bestimmten DMO kennen, den Sie verwenden möchten, können Sie den DMO Wrapper-Filter wie folgt mit diesem DMO initialisieren:

1.  Rufen **Sie CoCreateInstance auf,** um den DMO Wrapperfilter zu erstellen.
2.  Fragen Sie DMO Wrapperfilter für die [**IDMOWrapperFilter-Schnittstelle**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) ab.
3.  Rufen Sie die [**IDMOWrapperFilter::Init-Methode**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) auf. Geben Sie die CLSID des DMO und die GUID der Kategorie DMO an. Eine Liste der DMO finden Sie unter DMO [GUIDs](dmo-guids.md).

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



Die [**DMOEnum-Funktion**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) aufzählt DMOs in der Registrierung. Diese Funktion verwendet einen anderen Satz von Kategorie-GUIDs als diejenigen, die für DirectShow-Filter verwendet werden.

**Verwenden des Systemgeräte-Enumerators mit DMOs**

Anstatt einen DMO direkt zu erstellen, können Sie den [Systemgeräte-Enumerator](system-device-enumerator.md)verwenden, der jede DMO-Kategorie aufzählen kann, die von der **DMOEnum-Methode unterstützt** wird. Der Systemgeräte-Enumerator enthält auch DMOs, wenn er bestimmte DirectShow-Filterkategorien auflistet. Die folgende Tabelle zeigt die Zuordnung zwischen DMO Kategorien und DirectShow-Kategorien.



| Bezeichnung | Wert |
|-----------------------------|--------------------------------|
| DMO Kategorie                | DirectShow-Entsprechung          |
| \_DMOCATEGORY-AUDIOENCODER \_ | CLSID \_ AudioCompressorCategory |
| \_DMOCATEGORY-AUDIODECODER \_ | CLSID \_ LegacyAmFilterCategory  |
| \_DMOCATEGORY-VIDEOENCODER \_ | CLSID \_ VideoCompressorCategory |
| \_DMOCATEGORY-VIDEODECODER \_ | CLSID \_ LegacyAmFilterCategory  |



 

Der Systemgeräte-Enumerator gibt eine Liste von Monikerobjekten zurück. Wenn der Moniker eine DMO darstellt, erstellt die **IMoniker::BindToObject-Methode** automatisch den DMO Wrapper-Filter und initialisiert ihn mit DMO. Daher ist die Tatsache, dass DMO beteiligt ist, für die Anwendung transparent. Weitere Informationen zur Verwendung des Systemgeräte-Enumerators finden Sie unter [Verwenden des Systemgeräte-Enumerators.](using-the-system-device-enumerator.md)

**Einschränkungen**

Es gibt einige Einschränkungen bei der Verwendung von DMOs in DirectShow:

-   Der DMO Wrapperfilter unterstützt keine DMOs mit null Eingaben, mehreren Eingaben oder null Ausgaben.
-   Alle Pinverbindungen auf dem DMO Wrapperfilter verwenden die [**IMemInputPin-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   DirectShow-Bearbeitungsdienste unterstützen keine DMO oder Übergänge.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DMOs](using-dmos.md)
</dt> </dl>

 

 



