---
description: 'Schritt 5:'
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 'Schritt 5: Speichern eines Zeigers auf den Filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217481"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Schritt 5: Speichern eines Zeigers auf den Filter

Überschreiben Sie die [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode, um einen Zeiger auf den Filter zu speichern. Im folgenden Beispiel wird der- *Punk* -Parameter für die benutzerdefinierte isationinterface des Filters abgefragt:


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



Weiter: [Schritt 6. Initialisieren Sie das Dialog](step-6--initialize-the-dialog.md)Feld.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



