---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate- \_ rückkehrelement-withincorrectparent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559852"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate- \_ rückkehrelement-withincorrectparent

## <a name="text"></a>Text

Aufrufen von accNavigate ((Live Search), 0, navDir \_ FirstChild), die (x-Gadget:///gadget.html) zurückgegeben haben, hat das falsche übergeordnete Element (null) zurückgegeben, \[ \] nicht (Live Suche)

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das untergeordnete Element aufgerufen wird, das von " [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) " zurückgegeben wird (mithilfe der \_ Navigations Konstanten navDir firstChild oder navDir \_ LastChild), stimmt das zurückgegebene übergeordnete Element nicht mit dem übergeordneten Element identisch, das im **accNavigate** -Aufruf angegeben wurde.

![Beispiel für eine ungültige MSAA-Implementierung, die ein falsches übergeordnetes Element zurückgibt.](images/accchecker-invalid-msaa-parent.png)

Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: get- \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




