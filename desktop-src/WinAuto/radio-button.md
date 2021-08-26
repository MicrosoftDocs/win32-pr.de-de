---
title: Optionsfeld (REFERENZ ZUM MSAA-UI-Element)
description: Optionsfelder werden verwendet, um eine von mehreren Optionen auszuwählen, in der Regel innerhalb eines Dialogfelds.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c560e4efa57790980d852ab2716248d5b1d7faff535592f3f2ca892f3dff0715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998140"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Optionsfeld (REFERENZ ZUM MSAA-UI-Element)

> [!Note]  
> In diesem Thema werden **Optionsfeldobjekte für** die MsAA-Benutzeroberflächenelementreferenz beschrieben. Das Erstellen von **Optionsfeldobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenzdokumentation für das benutzeroberflächenframework, das Sie verwenden.

 

Optionsfelder werden verwendet, um eine von mehreren Optionen auszuwählen, in der Regel innerhalb eines Dialogfelds. Ein Optionsfeld enthält einen kleinen Kreis mit Text daneben. Wenn diese Option ausgewählt ist, hat der Kreis einen kleineren, ausgefüllten Kreis. Wenn Sie eine Schaltfläche in einem Satz auswählen, wird die zuvor ausgewählte Schaltfläche deaktiviert, sodass nur eine der Optionen in der Gruppe gleichzeitig ausgewählt wird.

Der Name der Fensterklasse für ein Optionsfeld ist "BUTTON".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Optionsfeld unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Methode                                                                    | Kommentare                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Die [**accDoDefaultAction-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) klickt auf das Optionsfeld. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Optionsfeld unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DefaultAction-Eigenschaft** für ein Optionsfeld ist "Check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffsschlüssel des Optionsfelds, bei dem es sich um ein unterstrichenes Zeichen im Fenstertext des Steuerelements handelt. Diese Zeichenfolge enthält das an die Zeichenfolge "ALT+" angefügte Zugriffsschlüsselzeichen.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** wird aus dem Fenstertext (oder der Beschriftung) des Steuerelements ermittelt, der mit dem Optionsfeld angezeigt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das -Steuerelement verfügt.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ RADIOBUTTON.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md)STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM FOCUSED STATE \| [**\_ \_**](object-state-constants.md) SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ CHECKED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Kontrollkästchen**](check-box.md)
</dt> <dt>

[**Group Box**](group-box.md)
</dt> <dt>

[**Schaltfläche "Push"**](push-button.md)
</dt> </dl>

 

 





