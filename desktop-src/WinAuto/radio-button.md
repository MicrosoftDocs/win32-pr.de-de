---
title: Optionsfeld (MSAA UI Element Reference)
description: Options Felder werden verwendet, um eine von mehreren Optionen auszuwählen, in der Regel in einem Dialogfeld.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9766e85f530281e4f843c4d39fd41fe35d4fb620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708633"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Optionsfeld (MSAA UI Element Reference)

> [!Note]  
> In diesem Thema werden options **Feld Objekte für** den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Vorgehensweise **zum Erstellen von** Optionsfeld Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Options Felder werden verwendet, um eine von mehreren Optionen auszuwählen, in der Regel in einem Dialogfeld. Ein Optionsfeld enthält einen kleinen Kreis mit Text daneben. Wenn diese Option ausgewählt ist, verfügt der Kreis über einen kleineren, gefüllten Kreis. Wenn Sie eine Schaltfläche in einem Satz auswählen, wird die zuvor ausgewählte Schaltfläche deaktiviert, sodass nur eine der Optionen in der Gruppe gleichzeitig ausgewählt wird.

Der Fenster Klassenname für ein Optionsfeld ist "Schaltfläche".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Optionsfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:



| Methode                                                                    | Kommentare                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Die [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) -Methode klickt auf das Optionsfeld. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Optionsfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DEFAULTACTION** -Eigenschaft für ein Optionsfeld ist "Check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Options Felds, bei der es sich um ein unterstrichenes Zeichen im Fenster Text des Steuer Elements handelt. Diese Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft wird aus dem Fenster Text (oder der Beschriftung) des Steuer Elements abgerufen, der mit dem Optionsfeld angezeigt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist das Optionsfeld " [**Rollen \_ System \_**](object-roles.md)".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System mit nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) barem Zustands System \| mit System eigenem Integritäts [**\_ \_**](object-state-constants.md) Integritäts \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) Status für Integritäts Status<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Kontrollkästchen**](check-box.md)
</dt> <dt>

[**Gruppenfeld**](group-box.md)
</dt> <dt>

[**Pushtaste**](push-button.md)
</dt> </dl>

 

 





