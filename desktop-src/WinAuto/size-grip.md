---
title: Größen-Greifer (Referenz zum MSAA-UI-Element)
description: Der Größenziehpunkt ist ein spezieller Mauszeiger in der unteren rechten Ecke eines Fensters, mit dem ein Benutzer auf den Größenziehpunkt klicken und ziehen kann, um die Größe des Fensters zu ändern.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7315425720ddee8beaf0f7c1f1b2ecbd8ba0fada51e64dc70453f3bb477e1f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795644"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Größen-Greifer (Referenz zum MSAA-UI-Element)

Der Größenziehpunkt ist ein spezieller Mauszeiger in der unteren rechten Ecke eines Fensters, mit dem ein Benutzer auf den Größenziehpunkt klicken und ziehen kann, um die Größe des Fensters zu ändern.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Der Größen-Greifer unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Der Größen-Greifer unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                   | Kommentare                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | Die **Description-Eigenschaft** ist "Kann verwendet werden, um die Breite und Höhe eines Fensters zu ändern".                                                                                   |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | Die **Name-Eigenschaft** ist "Size box".                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | Das Fenster, das den Größen-Greifer enthält.                                                                                                                                |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ GRIP.**](object-roles.md)                                                                                  |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | Der Wert für die **State-Eigenschaft** ist 0 (null), was bedeutet, dass das Objekt sichtbar ist, oder [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Iaccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




