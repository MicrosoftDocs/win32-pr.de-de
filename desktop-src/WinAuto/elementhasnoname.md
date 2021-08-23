---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cde3597a0922159eb035e94e08691cf9d36a07f8a1c23ec0cb25280ab961faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829529"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Text

Element hat keinen Namen

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Ein Element hat keinen Namen. Beispielsweise ist accName für das Element nicht implementiert, und eine leere Zeichenfolge wird zurückgegeben, wenn die [**get \_ accName-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) verwendet wird, um den MSAA-Namen des Elements abzurufen.

Dieses Problem verursacht Probleme für Benutzer, die eine Sprachausgabe und Tastatur für die Navigation verwenden, da ein Element für den Benutzer möglicherweise falsch identifiziert wird.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Element oder das übergeordnete Element hat keinen Namen oder keine Bezeichnung.
-   Dem Element wird eine [**accRole zugewiesen,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) die darauf hindeutet, dass das Element einen Namen hat.
-   Das Element, das den Fokus besitzt, sollte den Fokus nicht erhalten. Beispielsweise eine Bezeichnung oder ein deaktiviertes Steuerelement.
-   Ein unsichtbares Steuerelement hat den Fokus erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




