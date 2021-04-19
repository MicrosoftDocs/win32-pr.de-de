---
description: Schritt 9
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Schritt 9 Trennen der Eigenschaften Seite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356963"
---
# <a name="step-9-disconnect-the-property-page"></a>Schritt 9 Trennen der Eigenschaften Seite

Überschreiben Sie die [**cbasepropertypage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) -Methode, um alle Schnittstellen freizugeben, die Sie in der **OnConnect** -Methode abgerufen haben. Wenn der Benutzer das Eigenschaften Blatt schließt, ohne die Änderungen zu übernehmen, sollten Sie außerdem die ursprünglichen Werte wiederherstellen, wenn Sie sich geändert haben. Es gibt keine "OnCancel"-Methode, die aufgerufen wird, wenn der Benutzer abbricht, sodass Sie nachverfolgen müssen, ob der Benutzer " **onapplychanges**" aufgerufen hat. In diesem Beispiel wird die oben \_ beschriebene m LVAL-Variable verwendet:


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



Weiter: [Schritt 10. COM-Registrierung unterstützen](step-10--support-com-registration.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



