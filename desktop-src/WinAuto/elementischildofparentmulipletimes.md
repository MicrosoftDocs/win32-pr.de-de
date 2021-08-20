---
title: ElementIsChildOfParentMmupleTimes
description: ElementIsChildOfParentMmupleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfed0716423d8b1fef182be7cb0cb8ef122cf70cff6a574069fe40b63549f744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829549"
---
# <a name="elementischildofparentmulipletimes"></a>ElementIsChildOfParentMmupleTimes

## <a name="text"></a>Text

AccParent des Elements ist ( {0} ), aber das ursprüngliche Element ist ein untergeordnetes {1} Element.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das Zielelement aufgerufen wird, meldet es mehrmals, dass es ein untergeordnetes Element desselben übergeordneten Elements ist.

Dieses Problem kann zu Navigationsproblemen für automatisierte Tools führen, da das Durchlaufen von Elementen möglicherweise unvorhergesehen und unvorhersehbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




