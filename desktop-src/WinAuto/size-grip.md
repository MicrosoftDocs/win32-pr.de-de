---
title: Größen Zieh Punkt (MSAA UI-Element Referenz)
description: Der Größen Zieh Punkt ist ein spezieller Mauszeiger in der unteren rechten Ecke eines Fensters, in dem ein Benutzer auf den Größen Zieh Punkt klicken und ihn ziehen kann, um die Größe des Fensters zu ändern.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714135"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Größen Zieh Punkt (MSAA UI-Element Referenz)

Der Größen Zieh Punkt ist ein spezieller Mauszeiger in der unteren rechten Ecke eines Fensters, in dem ein Benutzer auf den Größen Zieh Punkt klicken und ihn ziehen kann, um die Größe des Fensters zu ändern.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Der Größen Zieh Punkt unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Der Größen Zieh Punkt unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                   | Kommentare                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | Die **Description** -Eigenschaft ist "kann verwendet werden, um die Breite und Höhe eines Fensters zu ändern".                                                                                   |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | Die **Name** -Eigenschaft ist "Size Box".                                                                                                                                   |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | Das Fenster, das den Größen Zieh Punkt enthält.                                                                                                                                |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | Die **Role** -Eigenschaft ist ein [**Rollen \_ System \_**](object-roles.md)-Ziehpunkt.                                                                                  |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | Der Wert für die **State** -Eigenschaft ist 0 (null), was bedeutet, dass das Objekt sichtbar ist oder das [**Zustands \_ System \_ unsichtbar**](object-state-constants.md)ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




