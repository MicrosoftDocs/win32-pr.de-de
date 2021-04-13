---
title: Elementisnotchildofelementsparent
description: Elementisnotchildofelementsparent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388795"
---
# <a name="elementisnotchildofelementsparent"></a>Elementisnotchildofelementsparent

## <a name="text"></a>Text

Das Element ist kein untergeordnetes Element des übergeordneten Elements.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das untergeordnete Element aufgerufen wird, das von " [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) " zurückgegeben wird (mithilfe der \_ Navigations Konstanten navDir firstChild oder navDir \_ LastChild), stimmt das zurückgegebene übergeordnete Element nicht mit dem übergeordneten Element identisch, das im **accNavigate** -Aufruf angegeben wurde.

Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: get- \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




