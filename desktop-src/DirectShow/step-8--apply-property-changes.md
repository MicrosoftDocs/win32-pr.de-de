---
description: 'Schritt 8:'
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 'Schritt 8: Anwenden von Eigenschaftsänderungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652056"
---
# <a name="step-8-apply-property-changes"></a>Schritt 8: Anwenden von Eigenschaftsänderungen

Überschreiben Sie [**die CBasePropertyPage::OnApplyChanges-Methode,**](cbasepropertypage-onapplychanges.md) um alle Eigenschaftsänderungen zu commiten. In diesem Beispiel wird die Variable m lNewVal immer dann aktualisiert, wenn der Benutzer auf der \_ Schiebereglerleiste scrollt. Die **OnApplyChanges-Methode** kopiert diesen Wert in die m \_ lVal-Variable und überschreiben den ursprünglichen Wert:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Weiter: [Schritt 9. Trennen Sie die Eigenschaftenseite](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftsseite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



