---
description: PIN-Eigenschaften Satz
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: PIN-Eigenschaften Satz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392505"
---
# <a name="pin-property-set"></a>PIN-Eigenschaften Satz

Der PIN-Eigenschaften Satz gibt die PIN-Kategorie für eine PIN in einem Filter zurück. Die Kategorie wird vom Filter festgelegt, wenn die PIN erstellt wird. die Kategorie gibt an, welche Art von Daten die PIN übermittelt oder von dieser Pin empfangen wird.



|                   |                      |
|-------------------|----------------------|
| Eigenschaftensatz-GUID | **Ampropeltid- \_ PIN** |



 



| Eigenschafts-ID                   | BESCHREIBUNG                      |
|-------------------------------|----------------------------------|
| **amproperty- \_ Pin- \_ Kategorie** | Gibt die Kategorie einer PIN an. |



 

DirectShow definiert die folgenden Pin-Kategorien in der Header Datei "UUIDs. h".



| Kategorie-GUID                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PIN- \_ Kategorie \_ Analog gvideoin**  | Eingabepin des Erfassungs Filters, der die Analogie annimmt und Sie standardisiert.                                                                                                                                                                                                                                                     |
| **Erfassung der PIN- \_ Kategorie \_**        | PIN erfassen.                                                                                                                                                                                                                                                                                                            |
| **PIN- \_ Kategorie \_ CC**             | PIN, die Untertitel Daten aus Zeile 21 bereitstellt.                                                                                                                                                                                                                                                                      |
| **PIN- \_ Kategorie \_ EDS**            | PIN, die erweiterte Data Services bereitstellt (Zeile 21, sogar Felder).                                                                                                                                                                                                                                                            |
| **anheften der \_ Kategorie \_**          | PIN, die Nordamerika-Videotext-Standard Daten bereitstellt.                                                                                                                                                                                                                                                                   |
| **\_Kategorie \_ Vorschau anheften**        | Vorschau der PIN.                                                                                                                                                                                                                                                                                                            |
| **PIN- \_ Kategorie \_ immer noch**          | PIN, die ein Bild enthält. Die Erfassungs-PIN des Filters muss verbunden sein, bevor die PIN mit dem Bild "immer noch" verbunden ist.                                                                                                                                                                                                    |
| **Kategorieinformationen für die PIN \_ \_**       | PIN, die Teletext bereitstellt (eine Untertitel Variante).                                                                                                                                                                                                                                                                   |
| **\_ \_ Zeit Leitzahl der PIN-Kategorie**       | PIN, die Zeit Code Daten bereitstellt.                                                                                                                                                                                                                                                                                            |
| **PIN- \_ Kategorie \_ VBI**            | Pin zur Bereitstellung vertikaler blankinginterval-Daten.                                                                                                                                                                                                                                                                          |
| **PIN- \_ Kategorie \_ Videoport**      | Die Video Ausgabe-PIN, die mit der Eingabe-PIN NULL auf dem [Überlagerungs Mixer](overlay-mixer-filter.md)verbunden werden soll                                                                                                                                                                                                                    |
| **PIN- \_ Kategorie \_ Videoport \_ VBI** | Anheften an den [VBI Surface Allocator](vbi-surface-allocator.md), den VBI Surface Allocator-Filter, der benötigt wird, um den korrekten Videospeicher für Dinge wie Untertitel Überschriften in Szenarios zuzuordnen, in denen ein Videoport verwendet wird. Dieser Filter wird von PCI-, IEEE 1394-und USB-Szenarien nicht verwendet. |
| **Pinname \_ Video \_ CC \_ Capture**   | Hardware Aufteilung mit Untertitel                                                                                                                                                                                                                                                                                  |



 

Diese Eigenschaft ist schreibgeschützt.

### <a name="example-code"></a>Beispielcode

Der folgende Code zeigt, wie Sie überprüfen können, ob eine PIN diesen Eigenschaften Satz unterstützt, und wenn dies der Fall ist, wie Sie die PIN-Kategorie abrufen:


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> In diesem Beispiel wird die Funktion " [saferelease](../medfound/saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PIN-Anforderungen für Erfassungs Filter](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Arbeiten mit PIN-Kategorien](working-with-pin-categories.md)
</dt> </dl>

 

 
