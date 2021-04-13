---
title: Elementhasnoname
description: Elementhasnoname
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311525"
---
# <a name="elementhasnoname"></a>Elementhasnoname

## <a name="text"></a>Text

Das Element hat keinen Namen.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element hat keinen Namen. Beispielsweise ist für das-Element der accName nicht implementiert, und eine leere Zeichenfolge wird zurückgegeben, wenn die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode verwendet wird, um den MSAA-Namen des Elements abzurufen.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element für den Benutzer fälschlicherweise identifiziert werden kann.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Element oder das übergeordnete Element hat keinen Namen oder keine Bezeichnung.
-   Dem-Element wird eine [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) zugewiesen, die vorschlägt, dass das Element einen Namen hat.
-   Das Element, das den Fokus besitzt, sollte keinen Fokus erhalten. Beispielsweise eine Bezeichnung oder ein deaktiviertes Steuerelement.
-   Ein unsichtbares Steuerelement hat den Fokus erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




