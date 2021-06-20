---
description: Speichern Sie einen Zeiger auf einen Filter als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 'Schritt 5: Speichern eines Zeigers auf den Filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406793"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Schritt 5: Speichern eines Zeigers auf den Filter

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

 

 



