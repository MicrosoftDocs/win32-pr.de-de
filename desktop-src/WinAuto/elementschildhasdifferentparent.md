---
title: Elementschildhasdifferenentparent
description: Elementschildhasdifferenentparent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311520"
---
# <a name="elementschildhasdifferentparent"></a>Elementschildhasdifferenentparent

## <a name="text"></a>Text

Das untergeordnete Element () des Elements {0} hat ein anderes {1} übergeordnetes Element () als Element

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler zeigt an, dass die untergeordneten Elemente, wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für die untergeordneten Elemente des Target-Elements aufgerufen wird, kein konsistentes übergeordnetes Element melden.

![ein Beispiel für die untergeordneten Elemente eines Elements, das eine inkonsistente übergeordnete Meldung meldet](images/accchecker-inconsistent-parent.png)

Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Accessiblechildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




