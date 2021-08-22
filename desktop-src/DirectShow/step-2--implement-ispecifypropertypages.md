---
description: Implementieren Sie die ISpecifyPropertyPages-Schnittstelle im Filter als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 'Schritt 2: Implementieren von ISpecifyPropertyPages'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2d1df86ef6e8b3e59f14a3efe1708a286761c9ba6425a7710a692ed6dcd3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951849"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Schritt 2: Implementieren von ISpecifyPropertyPages

Implementieren Sie als Nächstes die **ISpecifyPropertyPages-Schnittstelle** in Ihrem Filter. Diese Schnittstelle verfügt über eine einzelne Methode, **GetPages,** die ein Array von CLSIDs für die Eigenschaftenseiten zurückgibt, die der Filter unterstützt. In diesem Beispiel verfügt der Filter über eine einzelne Eigenschaftenseite. Generieren Sie zunächst die CLSID, und deklarieren Sie sie in Ihrer Headerdatei:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Implementieren Sie nun die **GetPages-Methode:**


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



Zuordnen von Arbeitsspeicher für das Array mithilfe von **CoTaskMemAlloc.** Der Aufrufer gibt den Arbeitsspeicher frei.

Weiter: [Schritt 3. Unterstützung von QueryInterface.](step-3--support-queryinterface.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftenseite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



