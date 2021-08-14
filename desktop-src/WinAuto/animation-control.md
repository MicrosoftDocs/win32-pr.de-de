---
title: Animationssteuerelement (REFERENZ ZUM MSAA-UI-Element)
description: Animationssteuerelemente zeigen automatisch einen zwischengespeicherten Audiovideoclip (AVI) an. Animationssteuerelemente werden normalerweise angezeigt, wenn Dateien kopiert werden oder wenn eine andere zeitaufwändige Aufgabe ausgeführt wird.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c7f134d5acdd3496f76e3399e5aafd1fcb2664aed37e042bb7c2cfca60f922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326854"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Animationssteuerelement (REFERENZ ZUM MSAA-UI-Element)

Animationssteuerelemente zeigen automatisch einen zwischengespeicherten Audiovideoclip (AVI) an. Animationssteuerelemente werden normalerweise angezeigt, wenn Dateien kopiert werden oder wenn eine andere zeitaufwändige Aufgabe ausgeführt wird.

Der Name der Fensterklasse für ein Animationssteuer steuerelement ist ANIMATE CLASS, die \_ in Commctrl.h als "SysAnimate32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Animationssteuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Animationssteuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Animationssteuerelemente verfügen nicht über Tastenkombinationen. Wenn die Bezeichnung für das Steuerelement jedoch einen Zugriffsschlüssel enthält (ein unterstrichenes Zeichen im Text der Bezeichnung des Steuerelements), gibt [**\_ get accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) eine Zeichenfolge zurück, die nicht NULL ist. Diese Zeichenfolge enthält das an die Zeichenfolge "ALT+" angefügte Zugriffsschlüsselzeichen. Wenn die Bezeichnung beispielsweise "Dateien herunterladen" ist, **ist KeyboardShortcut** "Alt+d".                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** wird aus dem statischen Textsteuerfeld erhalten, das das Animationssteuerfeld bezeichnet. Beim Erstellen von Steuerelementen müssen Serverentwickler sicherstellen, dass ein statisches Textsteuerfeld unmittelbar vor dem Steuerelement ausgeführt wird, das in der Registerkartenfolge bezeichnet wird.                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das -Steuerelement verfügt.                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ ANIMATION.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus mindestens einer der folgenden Objektzustandskonst constants: [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md)<br/> Weitere Informationen finden Sie unter [Objektzustandskonst constants](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





