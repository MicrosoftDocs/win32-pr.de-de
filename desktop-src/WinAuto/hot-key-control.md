---
title: Hot Key-Steuerelement (MSAA UI-Elementreferenz)
description: Mit Steuerelementen für heiße Schlüssel können Benutzer eine Kombination von Tastatureingaben eingeben, die als Hot-Key verwendet werden, sodass sie schnell eine Aktion ausführen können. Ein Hot-Key-Steuerelement zeigt die vom Benutzer eingegebenen Tastatureingaben an und stellt sicher, dass der Benutzer eine gültige Tastenkombination auswählt.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53829b371ea026c92388e8ed0dac11ee0303514ff930ad1a64ada4b5583bfa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734440"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Hot Key-Steuerelement (MSAA UI-Elementreferenz)

Mit Steuerelementen für heiße Schlüssel können Benutzer eine Kombination von Tastatureingaben eingeben, die als Hot-Key verwendet werden, sodass sie schnell eine Aktion ausführen können. Ein Hot-Key-Steuerelement zeigt die vom Benutzer eingegebenen Tastatureingaben an und stellt sicher, dass der Benutzer eine gültige Tastenkombination auswählt.

Der Fensterklassenname für ein HotKey-Steuerelement ist HOTKEY \_ CLASS, die in Commctrl.h als "msctls \_ hotkey32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Hot-Key-Steuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Die Hot-Tasten-Steuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist immer 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffstaste des Steuerelements für die heiße Taste, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung des Steuerelements mit der heißen Taste handelt. Die zurückgegebene Zeichenfolge enthält das Anfügen des Zugriffsschlüsselzeichens an die Zeichenfolge "ALT+".                                                                                                                                                                                                                                 |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** ist der Text aus einem statischen Textsteuerelement, das das Hot-Key-Steuerelement bezeichnet.                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das Steuerelement verfügt.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ HOTKEYFIELD.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Die **Value-Eigenschaft** ist eine Zeichenfolge, die den Text im Hot Key-Feld enthält.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





