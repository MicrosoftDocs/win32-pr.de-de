---
description: 'Schritt 2:'
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 'Schritt 2: Implementieren von ISpecifyPropertyPages'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352432"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Schritt 2: Implementieren von ISpecifyPropertyPages

Implementieren Sie als nächstes die **ISpecifyPropertyPages** -Schnittstelle in Ihrem Filter. Diese Schnittstelle verfügt über eine einzelne Methode, **GetPages**, die ein Array von CLSIDs für die Eigenschaften Seiten zurückgibt, die der Filter unterstützt. In diesem Beispiel verfügt der Filter über eine einzelne Eigenschaften Seite. Erstellen Sie zunächst die CLSID, und deklarieren Sie Sie in der Header Datei:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Implementieren Sie nun die **GetPages** -Methode:


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Zuweisen von Arbeitsspeicher für das Array mit " **CoTaskMemAlloc**". Der Aufrufer gibt den Arbeitsspeicher frei.

Weiter: [Schritt 3. Unterstützung von QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



