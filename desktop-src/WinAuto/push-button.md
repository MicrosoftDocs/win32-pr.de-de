---
title: Schaltfläche "Push" (Referenz zum MSAA-UI-Element)
description: Eine Schaltfläche ist ein kleines rechteckiges Objekt, das zum Ausführen einer Aktion verwendet wird. Beispielsweise sind die Schaltflächen OK und ABBRECHEn in einem Dialogfeld Schaltflächen.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4056b1b2bd8f80e79916db0056de176962bd7d3d86c2b62420deaf57f90e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644490"
---
# <a name="push-button-msaa-ui-element-reference"></a>Schaltfläche "Push" (Referenz zum MSAA-UI-Element)

Eine Schaltfläche ist ein kleines rechteckiges Objekt, das zum Ausführen einer Aktion verwendet wird. Beispielsweise sind die **Schaltflächen OK** **und ABBRECHEn** in einem Dialogfeld Schaltflächen.

Der Name der Fensterklasse für eine Pushschaltfläche ist "BUTTON".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Eine Pushschaltfläche unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Methode                                                                    | Kommentare                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Die [**accDoDefaultAction-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) klickt auf die Pushschaltfläche. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Eine Pushschaltfläche unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist 0 (null) oder mehr.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DefaultAction-Eigenschaft** ist "Press".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffsschlüssel der Schaltfläche, bei der es sich um ein unterstrichenes Zeichen im Text des Fenstertexts der Schaltfläche handelt. "Alt+o" ist z. B. die **KeyboardShortcut-Eigenschaft** für eine **SCHALTFLÄCHE OK.**                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** wird aus dem Fenstertext (oder der Beschriftung) des Steuerelements ermittelt, der in der Schaltfläche "Push" angezeigt wird. "OK" ist z. B. die **Name-Eigenschaft** für eine **OK-Schaltfläche.**                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das -Steuerelement verfügt.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ PUSHBUTTON.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md)STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM FOCUSED STATE \| [**\_ \_**](object-state-constants.md) SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PRESSED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ DEFAULT**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Kontrollkästchen**](check-box.md)
</dt> <dt>

[**Group Box**](group-box.md)
</dt> <dt>

[**Optionsfeld**](radio-button.md)
</dt> </dl>

 

 





