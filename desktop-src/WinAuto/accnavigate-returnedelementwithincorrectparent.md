---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd040cda80e9dcb19543c8ee5134271693546dfdb8af76053b5a281340080765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122465"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate \_ ReturnedElementWithIncorrectParent

## <a name="text"></a>Text

Der Aufruf von accNavigate((Live Search), 0, NAVDIR FIRSTCHILD), der (x-gadget:///gadget.html) zurückgibt, hat das falsche übergeordnete Element( NULL ) und nicht \_ \[ \] (Live Search) zurückgegeben.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das untergeordnete Element aufgerufen wird, das von [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) zurückgegeben wird (entweder mithilfe der Navigationskonstierten NAVDIR FIRSTCHILD oder NAVDIR LASTCHILD), ist das zurückgegebene übergeordnete Element nicht mit dem übergeordneten Element übereinstimmen, das im \_ \_ **accNavigate-Aufruf** angegeben ist.

![Beispiel für eine ungültige msaa-Implementierung, die ein falsches übergeordnetes Element zurückgibt.](images/accchecker-invalid-msaa-parent.png)

Dieses Problem kann zu Navigationsproblemen bei automatisierten Tools führen, da das Durchlaufen von Elementen möglicherweise unvorhergesehen und unvorhersehbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




