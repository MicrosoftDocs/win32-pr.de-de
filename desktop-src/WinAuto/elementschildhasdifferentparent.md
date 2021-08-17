---
title: ElementeChildHasDifferentParent
description: ElementeChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 885a5d930892d6e202764de8e58371f02690edee6715155f34533aaa110d7080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829184"
---
# <a name="elementschildhasdifferentparent"></a>ElementeChildHasDifferentParent

## <a name="text"></a>Text

Das untergeordnete Element {0} () des Elements hat ein anderes übergeordnetes Element( {1} ) als das Element.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gibt an, dass die übergeordneten Elemente kein konsistentes übergeordnetes Element melden, wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für die unteren Elemente des Zielelements aufgerufen wird.

![Beispiel für die unteren Elemente eines Elements, die ein inkonsistentes übergeordnetes Element melden](images/accchecker-inconsistent-parent.png)

Dieses Problem kann zu Navigationsproblemen für automatisierte Tools führen, da das Durchlaufen von Elementen möglicherweise unvorhergesehen und unvorhersehbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




