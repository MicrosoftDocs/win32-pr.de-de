---
description: Pin-Eigenschaftssatz
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Pin-Eigenschaftssatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909618"
---
# <a name="pin-property-set"></a>Pin-Eigenschaftssatz

Der Pin-Eigenschaftensatz gibt die Pinkategorie für eine Stecknadel in einem Filter zurück. Die Kategorie wird vom Filter festgelegt, wenn er die Stecknadel erstellt. Die Kategorie gibt an, welche Art von Daten der Pin von diesem Pin übermittelt oder empfängt.



| Bezeichnung | Wert |
|-------------------|----------------------|
| Eigenschaftensatz-GUID | **AMPROPSETID \_ Pin** |



 



| Eigenschafts-ID                   | BESCHREIBUNG                      |
|-------------------------------|----------------------------------|
| **\_AMPROPERTY-PIN-KATEGORIE \_** | Gibt die Kategorie eines Stecknadels an. |



 

DirectShow definiert die folgenden Pinkategorien in der Headerdatei "Uuids.h".



| Kategorie-GUID                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PINKATEGORIE \_ \_ ANALOGVIDEOIN**  | Eingabepin des Erfassungsfilters, der analog verwendet und digitalisiert.                                                                                                                                                                                                                                                     |
| **AUFNAHME DER \_ \_ PINKATEGORIE**        | Aufnahmepin.                                                                                                                                                                                                                                                                                                            |
| **PINKATEGORIE \_ \_ CC**             | Heften Sie die Untertiteldaten aus Zeile 21 an.                                                                                                                                                                                                                                                                      |
| **\_EDS DER \_ PIN-KATEGORIE**            | Pin für erweiterte Data Services (Zeile 21, sogar Felder).                                                                                                                                                                                                                                                            |
| **\_ \_ PIN-KATEGORIE -HEFTE**          | Heften Sie die Daten des Us-amerikanischen Videotext-Standards an.                                                                                                                                                                                                                                                                   |
| **\_VORSCHAU DER PIN-KATEGORIE \_**        | Vorschau-Stecknadel.                                                                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ STILL**          | Stecknadel, die ein Standbild bereitstellt. Der Erfassungspin des Filters muss verbunden sein, bevor der Pin für das Standbild verbunden ist.                                                                                                                                                                                                    |
| **PIN \_ CATEGORY \_ TELETEXT**       | Anheften der Bereitstellung von Teletext (eine Untertitelvariante).                                                                                                                                                                                                                                                                   |
| **PIN \_ CATEGORY \_ TIMECODE**       | Anheften der Bereitstellung von Zeitcodedaten.                                                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ VBI**            | Stecknadel, die Daten zum vertikalen Leerungsintervall bereitstellt.                                                                                                                                                                                                                                                                          |
| **PIN \_ CATEGORY \_ VIDEOPORT**      | Videoausgabepin, der mit dem Eingabepin 0 (null) auf dem [Overlay-Mixer](overlay-mixer-filter.md)verbunden werden soll.                                                                                                                                                                                                                    |
| **PIN \_ CATEGORY \_ VIDEOPORT \_ VBI** | Stecknadel für die Verbindung mit der [VBI-Oberflächenbelegung](vbi-surface-allocator.md), dem VBI-Oberflächenbelegungsfilter, der benötigt wird, um den richtigen Videospeicher für Dinge wie Untertitelüberlagerungen in Szenarien zuzuweisen, in denen ein Videoport verwendet wird. PCI-, IEEE 1394- und USB-Szenarien verwenden diesen Filter nicht. |
| **PINNAME \_ VIDEO \_ CC \_ CAPTURE**   | Hardwareslicing-Pin für Untertitel                                                                                                                                                                                                                                                                                  |



 

Diese Eigenschaft ist schreibgeschützt.

### <a name="example-code"></a>Beispielcode

Der folgende Code zeigt, wie Sie überprüfen, ob ein Pin diesen Eigenschaftensatz unterstützt, und wenn ja, wie Sie die Pinkategorie abrufen:


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
> In diesem Beispiel wird die [SafeRelease-Funktion](../medfound/saferelease.md) verwendet, um Schnittstellenzeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anheftanforderungen für Erfassungsfilter](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Arbeiten mit Pinkategorien](working-with-pin-categories.md)
</dt> </dl>

 

 
