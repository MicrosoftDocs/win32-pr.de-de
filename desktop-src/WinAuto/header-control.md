---
title: Header Steuer Element (MSAA UI-Element Referenz)
description: Ein Header Steuerelement zeigt Überschriften am oberen Rand der Spalten von Informationen an und ermöglicht dem Benutzer, die Informationen durch Klicken auf die Überschriften zu sortieren. Windows-Explorer verwendet ein Header-Steuerelement, wenn die Detailansicht ausgewählt wird.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310760"
---
# <a name="header-control-msaa-ui-element-reference"></a>Header Steuer Element (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Header Steuerungs** Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Vorgehensweise zum Erstellen von **Header Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Header Steuerelement zeigt Überschriften am oberen Rand der Spalten von Informationen an und ermöglicht dem Benutzer, die Informationen durch Klicken auf die Überschriften zu sortieren. Windows-Explorer verwendet ein Header-Steuerelement, wenn die Detailansicht ausgewählt wird.

Der Fenster Klassenname für ein Header Steuerelement ist ein WC- \_ Header, der in "kommctrl. h" als "SysHeader32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Header-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:



| Methode                                                                    | Kommentare                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Diese Methode führt die Standardaktion durch Klicken auf den Header aus. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Header-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                       | Kommentare                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                   |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Die **DEFAULTACTION** -Eigenschaft ist "Click".                                                                                                                                                                                             |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Die **Name** -Eigenschaft ist identisch mit dem Namen der Spaltenüberschrift.                                                                                                                                                                    |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Liste**](object-roles.md) ), das das Steuerelement umgibt und denselben Fenster Klassennamen wie das Steuerelement aufweist.                                                      |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Die **Role** -Eigenschaft ist [**Rollen \_ System- \_ ColumnHeader**](object-roles.md).                                                                                                                                  |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Der Wert für die **State** -Eigenschaft lautet [**immer \_ Zustands \_ System**](object-state-constants.md) schreibgeschützt und kann auch [**Status \_ System \_ unsichtbar**](object-state-constants.md)enthalten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




