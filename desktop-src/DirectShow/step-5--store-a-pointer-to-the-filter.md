---
description: Store einen Zeiger auf einen Filter als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 'Schritt 5: Store eines Zeigers auf den Filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63becf4cb98f401a4810f0f9a2604ef65387a58d08d84b9f670c09b51fe9acd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078770"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Schritt 5: Store eines Zeigers auf den Filter

Überschreiben Sie die [**CBasePropertyPage::OnConnect-Methode,**](cbasepropertypage-onconnect.md) um einen Zeiger auf den Filter zu speichern. Im folgenden Beispiel wird der *pUnk-Parameter* für die benutzerdefinierte ISaturation-Schnittstelle des Filters abgefragt:


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



Weiter: [Schritt 6. Initialisieren Sie das Dialogfeld](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftenseite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



