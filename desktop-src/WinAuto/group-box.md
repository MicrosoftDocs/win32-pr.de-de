---
title: Group Box (MSAA UI-Elementreferenz)
description: Ein Gruppenfeld ist ein Rechteck, das eine Reihe von Steuerelementen umschließt, z. B. Kontrollkästchen oder Optionsfelder, und einen anwendungsdefiniertem Text (Bezeichnung) enthält.
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06675a1ffa88e83bc3c5e36f5d8410682e797169b83e98aa1680b0f0c50d28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860320"
---
# <a name="group-box-msaa-ui-element-reference"></a>Group Box (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Group Box-Objekte** im Rahmen der MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Group Box-Objekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Ein Gruppenfeld ist ein Rechteck, das eine Reihe von Steuerelementen umschließt, z. B. Kontrollkästchen oder Optionsfelder, und einen anwendungsdefiniertem Text (Bezeichnung) enthält.

Der einzige Zweck eines Gruppenfelds besteht darin, Steuerelemente zu organisieren, die sich auf einen gemeinsamen Zweck beziehen, der durch die Bezeichnung angegeben wird.

Der Fensterklassenname für ein Gruppenfeld lautet "BUTTON".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Gruppenfeld unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Gruppenfeld unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist immer 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Gruppenfelder verfügen nicht über Tastenkombinationen. Wenn der Fenstertext für das Gruppenfeld jedoch ein ampersand-Zeichen (&) enthält, gibt Microsoft Active Accessibility eine Zeichenfolge ungleich NULL als **KeyboardShortcut-Eigenschaft** zurück.                                                                                                                                                                                                                                            |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** wird aus dem Fenstertext (oder der Beschriftung) des Steuerelements abgerufen, der mit dem Gruppenfeld angezeigt wird.                                                                                                                                                                                                                                                                                                                                                    |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das Steuerelement verfügt.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ GROUPING.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





