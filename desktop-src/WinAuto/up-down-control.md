---
title: Up-Down-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)
description: Ein auf-ab-Steuerelement, das auch als Dreh Steuerelement bezeichnet wird, kombiniert ein paar von Schaltflächen, die als Pfeile mit einem Buddy-Bearbeitungs Steuerelement angezeigt werden Durch Klicken auf die Pfeile wird der Wert im Bearbeitungs Steuerelement erhöht oder verringert.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd2d28acc4c14a89ec73f5994ed0af47202145a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342055"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Up-Down-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)

> [!Note]  
> In diesem Thema **werden auf-ab-Steuer** Element Objekten für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Informationen zum Erstellen von **auf-ab-Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks werden hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein auf-ab-Steuerelement, das auch als Dreh Steuerelement bezeichnet wird, kombiniert ein paar von Schaltflächen, die als Pfeile mit einem Buddy-Bearbeitungs Steuerelement angezeigt werden Durch Klicken auf die Pfeile wird der Wert im Bearbeitungs Steuerelement erhöht oder verringert.

Der Fenster Klassenname für ein auf-ab-Steuerelement ist eine UpDown- \_ Klasse, die in "commctrl. h" als "msctls \_ updown32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein auf-ab-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein auf-ab-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **childCount** -Eigenschaft ist "2" (die Pfeil Schaltflächen nach oben und nach unten).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name** -Eigenschaft für das auf-ab-Steuerelement wird aus dem Fenster Text (oder der Beschriftung) des Steuer Elements abgerufen. Dieser Text wird nicht mit dem auf-ab-Steuerelement angezeigt, sodass Server Entwickler sinnvollen Text in der Ressourcen Definitions Anweisung des Steuer Elements angeben müssen, damit Benutzer von Client Dienstprogrammen das Steuerelement identifizieren können. Die **Name** -Eigenschaft für die Schaltfläche mit dem Pfeil nach oben im auf-ab-Steuerelement ist "More", und die **Name** -Eigenschaft für die untere Pfeil Schaltfläche ist "less". |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent** -Eigenschaft des auf-ab-Steuer Elements ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist. Die über **geordnete** Eigenschaft der Pfeil Schaltflächen nach oben und nach unten ist das auf-ab-Steuerelement Objekt.                                                                                                                                                    |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft für das auf-ab-Steuerelement Objekt ist [**Rollen \_ System- \_ SpinButton**](object-roles.md). Die **Role** -Eigenschaft für die Pfeil Schaltflächen ist [**Rollen \_ System- \_ PUSHBUTTON**](object-roles.md).                                                                                                                                                                                                                          |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die State-Eigenschaft für das auf-ab-Steuerelement Objekt hat einen der folgenden [Werte](object-state-constants.md): Zustands System mit [**Fokus, \_ \_ Fokus**](object-state-constants.md) \| [**\_ \_ verwendbar**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**\_accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notizen

Microsoft Active Accessibility macht das Steuerelement "Buddy Edit" als separates Objekt verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





