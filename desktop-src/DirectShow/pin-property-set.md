---
description: Pin-Eigenschaftensatz
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Pin-Eigenschaftensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d143d980de7f2a634deecb2c3f06509854ac5a50fbe120da279cce3ad97be1e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316100"
---
# <a name="pin-property-set"></a>Pin-Eigenschaftensatz

Der Pin-Eigenschaftensatz gibt die Pinkategorie für eine Stecknadel in einem Filter zurück. Die Kategorie wird vom Filter beim Erstellen des Pins festgelegt. Die Kategorie gibt an, welche Art von Daten der Pin von diesem Pin übermittelt oder empfängt.



| Bezeichnung | Wert |
|-------------------|----------------------|
| Eigenschaftensatz-GUID | **AMPROPSETID \_ Pin** |



 



| Eigenschafts-ID                   | BESCHREIBUNG                      |
|-------------------------------|----------------------------------|
| **\_AMPROPERTY-PIN-KATEGORIE \_** | Gibt die Kategorie eines Pins an. |



 

DirectShow definiert die folgenden Pinkategorien in der Headerdatei "Uuids.h".



| Kategorie-GUID                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PINKATEGORIE \_ \_ ANALOGVIDEOIN**  | Eingabepin des Erfassungsfilters, der analog verwendet und digitalisiert.                                                                                                                                                                                                                                                     |
| **AUFNAHME DER \_ \_ PINKATEGORIE**        | Aufnahmepin.                                                                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ CC**             | Heften Sie die Untertiteldaten aus Zeile 21 an.                                                                                                                                                                                                                                                                      |
| **\_EDS DER \_ PIN-KATEGORIE**            | Pin für erweiterte Data Services (Zeile 21, sogar Felder).                                                                                                                                                                                                                                                            |
| **\_ \_ PIN-KATEGORIE -HEFTE**          | Heften Sie die Daten des North American Videotext Standard an.                                                                                                                                                                                                                                                                   |
| **PIN \_ CATEGORY \_ PREVIEW**        | Vorschaupin.                                                                                                                                                                                                                                                                                                            |
| **\_ \_ PIN-KATEGORIE NOCH**          | Stecknadel, die ein Stillbild bietet. Der Erfassungspin des Filters muss verbunden sein, bevor der Stift für das Stillbild verbunden wird.                                                                                                                                                                                                    |
| **PIN \_ CATEGORY \_ TELETEXT**       | Anheften des Teletexts (eine Untertitelvariante).                                                                                                                                                                                                                                                                   |
| **PIN \_ CATEGORY \_ TIMECODE**       | Pin zur Angabe von Zeitcodedaten.                                                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ VBI**            | Anheften, das daten zum vertikalen Leerungsintervall anheften.                                                                                                                                                                                                                                                                          |
| **PIN \_ CATEGORY \_ VIDEOPORT**      | Videoausgabepin, der mit dem Eingabepin 0 (null) auf dem Overlay-Gerät verbunden [Mixer.](overlay-mixer-filter.md)                                                                                                                                                                                                                    |
| **PIN \_ CATEGORY \_ VIDEOPORT \_ VBI** | Pin, der mit der [VBI Surface Allocator](vbi-surface-allocator.md)verbunden werden soll, dem VBI-Oberflächenzuweisungsfilter, der zum Zuordnen des richtigen Videospeichers für Dinge wie Untertitelüberlagerungen in Szenarien erforderlich ist, in denen ein Videoport verwendet wird. PCI-, IEEE 1394- und USB-Szenarien verwenden diesen Filter nicht. |
| **PINNAME \_ VIDEO \_ CC \_ CAPTURE**   | Hardwareslicing-Pin für Untertitel                                                                                                                                                                                                                                                                                  |



 

Diese Eigenschaft ist schreibgeschützt.

### <a name="example-code"></a>Beispielcode

Der folgende Code zeigt, wie Überprüft wird, ob eine Stecknadel diesen Eigenschaftensatz unterstützt, und wenn dies der Fall ist, wie die Stecknadelkategorie erhalten wird:


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
> In diesem Beispiel wird die [SafeRelease-Funktion verwendet,](../medfound/saferelease.md) um Schnittstellenzeigen zu veröffentlichen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anheftanforderungen für Erfassungsfilter](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Arbeiten mit Pinkategorien](working-with-pin-categories.md)
</dt> </dl>

 

 
