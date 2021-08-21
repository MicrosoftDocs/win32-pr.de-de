---
title: Statischer Text (REFERENZ ZUM MSAA-UI-Element)
description: Statische Textsteuerelemente bieten eine praktische Möglichkeit, Text in Dialogfeldern und anderen Fenstern anzuzeigen. Statische Textsteuerelemente dienen häufig als Bezeichnungen für andere Steuerelemente.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da892a102caa8a1af1729bdb4fc2258f461828adf1f7622e8ff5abf8a2a0bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052488"
---
# <a name="static-text-msaa-ui-element-reference"></a>Statischer Text (REFERENZ ZUM MSAA-UI-Element)

Statische Textsteuerelemente bieten eine praktische Möglichkeit, Text in Dialogfeldern und anderen Fenstern anzuzeigen. Statische Textsteuerelemente dienen häufig als Bezeichnungen für andere Steuerelemente.

Der Fensterklassenname für ein statisches Textsteuerfeld ist "STATIC".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Statische Textsteuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Statische Textsteuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                                                                                          |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffsschlüssel, bei der es sich um das unterstrichene Zeichen im Text handelt, das das steuerelement aktiviert, das dem statischen Text zugeordnet ist. Die zurückgegebene Zeichenfolge enthält das an die Zeichenfolge "ALT+" angefügte Zugriffsschlüsselzeichen.                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** ist identisch mit dem Text im statischen Textsteuerfeld.                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das -Steuerelement verfügt.                                                                                   |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ STATICTEXT.**](object-roles.md)                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md) [**STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Hinweise

-   Die [**accSelect-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) gibt DISP E MEMBERNOTFOUND zurück, wenn sie mit \_ \_ [**SELFLAG \_ TAKEFOCUS**](selflag.md) für ein statisches Textobjekt aufgerufen wird.
-   Statische Steuerelemente mit dem SS \_ ICON-Stil geben ungültige Daten in der **Name-Eigenschaft** zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





