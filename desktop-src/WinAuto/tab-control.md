---
title: Registerkarten-Steuer Element (MSAA UI-Element Referenz)
description: Ein Registerkarten-Steuerelement definiert mehrere Seiten für denselben Bereich eines Fensters oder Dialog Felds.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cc8381a668701446e06df81694941ece9f5f259
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338983"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Registerkarten-Steuer Element (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden Registerkarten- **Steuer** Element Objekte zum Zweck der MSAA-Benutzeroberflächen Element Referenz beschrieben. Die Vorgehensweise zum Erstellen von **Register Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Registerkarten-Steuerelement definiert mehrere Seiten für denselben Bereich eines Fensters oder Dialog Felds. Jede Seite besteht aus einem Satz von Informationen oder einer Gruppe von Steuerelementen, die von einer Anwendung angezeigt werden, wenn der Benutzer die entsprechende Registerkarte auswählt. Das Windows-Betriebssystem verwendet Registerkarten-Steuerelemente, um die Task leisten Schaltflächen mit Ausnahme der Schaltfläche **Start** anzuzeigen.

Der Fenster Klassenname für ein Registerkarten-Steuerelement ist \_ "WC TabControl", das in "commctrl. h" als "systabcontrol" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Registerkarten-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:



| Methode                                                                    | Kommentare                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Die [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) -Methode klickt auf die Registerkarte "Seite". |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Registerkarten-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DEFAULTACTION** -Eigenschaft ist "Switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Register Steuer Elements, bei der es sich um ein unterstrichenes Zeichen im Fenster Text des Steuer Elements handelt. Diese Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft wird aus dem Fenster Text (oder der Beschriftung) des Steuer Elements abgerufen, der im Registerkarten-Steuerelement angezeigt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster [**( \_ \_ pagetablist**](object-roles.md) ), das das Steuerelement umgibt und denselben Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist [**role \_ System \_ pgetab**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**\_Zugriffs Auswahl**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System- [**\_ \_**](object-state-constants.md) \| [**\_ \_ auswählbares**](object-state-constants.md) Zustands System System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ aktiviertem**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) Zustands System<br/> |



 

## <a name="notes"></a>Notizen

Registerkarten-Steuerelemente geben bei Aufrufen \_ mit dem selflag-Flag " [**\_ TakeFocus**](selflag.md) " fälschlicherweise den Wert von "S OK" zurück. [](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) Registerkarten-Steuerelemente können den Tastaturfokus nicht annehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





