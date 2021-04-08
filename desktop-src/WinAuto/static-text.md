---
title: Statischer Text (MSAA UI-Element Referenz)
description: Statische Text Steuerelemente bieten eine bequeme Möglichkeit, Text in Dialogfeldern und anderen Fenstern anzuzeigen. Statische Text Steuerelemente dienen oft als Bezeichnungen für andere Steuerelemente.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856859"
---
# <a name="static-text-msaa-ui-element-reference"></a>Statischer Text (MSAA UI-Element Referenz)

Statische Text Steuerelemente bieten eine bequeme Möglichkeit, Text in Dialogfeldern und anderen Fenstern anzuzeigen. Statische Text Steuerelemente dienen oft als Bezeichnungen für andere Steuerelemente.

Der Fenster Klassenname für ein statisches Text Steuerelement ist "static".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Statische Text Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Statische Text Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                                                                          |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste, bei der es sich um das unterstrichene Zeichen im Text handelt, das das dem statischen Text zugeordnete Steuerelement aktiviert. Die zurückgegebene Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.                                           |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft entspricht dem Text im statischen Text Steuerelement.                                                                                                                                                                                                                     |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                   |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist [**role \_ System \_ StaticText**](object-roles.md).                                                                                                                                                                                             |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): [**Zustands \_ \_**](object-state-constants.md) System Schreib geschütztes \| [**Zustands \_ System \_ unsichtbar**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notizen

-   Die Methode [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) gibt DISP \_ E \_ mitgliednotfound zurück, wenn Sie mit [**selflag \_ TakeFocus**](selflag.md) für ein statisches Textobjekt aufgerufen wird.
-   Statische Steuerelemente mit dem SS- \_ Symbolstil geben ungültige Daten in der **Name** -Eigenschaft zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





