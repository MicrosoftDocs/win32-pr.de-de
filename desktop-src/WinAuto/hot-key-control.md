---
title: Hot Key-Steuer Element (MSAA-Benutzeroberflächen-Element Referenz)
description: Mithilfe von Hot Key-Steuerelementen können Benutzer eine Kombination von Tastatureingaben eingeben, die als heiße Taste verwendet werden, sodass Sie schnell eine Aktion ausführen können. Ein Hot Key-Steuerelement zeigt die vom Benutzer eingegebenen Tastatureingaben an und stellt sicher, dass der Benutzer eine gültige Tastenkombination auswählt.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aed12ce64fe25c091f6204d9143a0c6ebefb65a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310759"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Hot Key-Steuer Element (MSAA-Benutzeroberflächen-Element Referenz)

Mithilfe von Hot Key-Steuerelementen können Benutzer eine Kombination von Tastatureingaben eingeben, die als heiße Taste verwendet werden, sodass Sie schnell eine Aktion ausführen können. Ein Hot Key-Steuerelement zeigt die vom Benutzer eingegebenen Tastatureingaben an und stellt sicher, dass der Benutzer eine gültige Tastenkombination auswählt.

Der Fenster Klassenname für ein Hot Key-Steuerelement ist eine Hotkey- \_ Klasse, die in "commctrl. h" als "msctls \_ hotkey32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Hot Key-Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Die Hot Key-Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist immer 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Hot Key-Steuer Elements, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung des Hot Key-Steuer Elements handelt. Die zurückgegebene Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.                                                                                                                                                                                                                                 |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft ist der Text aus einem statischen Text Steuerelement, das das Steuerelement für den Abkürzungs Schlüssel bezeichnet                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                              |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist das [**Rollen \_ System- \_ hotkeyfield**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |
| [**\_accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Die **value** -Eigenschaft ist eine Zeichenfolge, die den Text im Feld "Hot Key" enthält.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





