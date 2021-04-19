---
description: 'Schritt 8:'
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 'Schritt 8: Anwenden von Eigenschafts Änderungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359450"
---
# <a name="step-8-apply-property-changes"></a>Schritt 8: Anwenden von Eigenschafts Änderungen

Überschreiben Sie die [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md) -Methode, um einen Commit für alle Eigenschafts Änderungen vorzunehmen. In diesem Beispiel wird die m \_ lnewval-Variable immer dann aktualisiert, wenn der Benutzer den Schieberegler durchläuft. Die **onapplychanges** -Methode kopiert diesen Wert in die m \_ LVAL-Variable, wobei der ursprüngliche Wert überschrieben wird:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Weiter: [Schritt 9. Trennen Sie die Eigenschaften Seite](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



