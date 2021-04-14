---
title: Nullparent
description: Nullparent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309868"
---
# <a name="nullparent"></a>Nullparent

## <a name="text"></a>Text

Das übergeordnete Element ist NULL.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

NULL wird zurückgegeben, wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das Element aufgerufen wird. Die **get \_ accParent** -Methode sollte NULL nur zurückgeben, wenn Sie für das Stamm Element des Überprüfungs Ziels aufgerufen wird.

Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: get- \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




