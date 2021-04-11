---
title: StatusBar-Steuer Element (MSAA UI-Element Referenz)
description: In Status leisten werden Statusinformationen in einem horizontalen Fenster am unteren Rand eines Anwendungsfensters angezeigt.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311202"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>StatusBar-Steuer Element (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **StatusBar-Steuer** Element Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von **StatusBar-Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

In Status leisten werden Statusinformationen in einem horizontalen Fenster am unteren Rand eines Anwendungsfensters angezeigt. Status leisten sind häufig in Teile unterteilt, die als Bereiche bezeichnet werden, und in jedem Bereich werden andere Statusinformationen angezeigt. Außerdem können Status leisten Objekte unterschiedlicher Typen enthalten, einschließlich Schaltflächen und Status leisten. Der Fenster Klassenname für ein StatusBar-Steuerelement ist statusclassname, das in der Datei "kommctrl. h" als "msctls \_ statusbar32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Status leisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Status leisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **childCount** -Eigenschaft ist die Anzahl der Bereiche in der Statusleiste.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Das StatusBar-Objekt selbst hat keine **Name** -Eigenschaft. Die **Name** -Eigenschaft jedes Bereichs in der Statusleiste ist mit dem angezeigten Text identisch.                                                                                                                                                                                                                                                                                                                   |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent** -Eigenschaft des StatusBar-Objekts ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und denselben Fenster Klassennamen wie das Steuerelement aufweist. Die über **geordnete** Eigenschaft der Bereiche in der Statusleiste ist das StatusBar-Objekt.                                                                                                                                                                           |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft für das StatusBar-Objekt selbst ist [**role \_ System \_ StatusBar**](object-roles.md). Der in einer Statusleiste angezeigte Text verfügt über das [**role \_ System \_ StaticText**](object-roles.md) als seine **Role** -Eigenschaft.                                                                                                                                                                                                 |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notizen

Da Tastenkombinationen für StatusBar-Steuerelemente oder Textbereiche in Status leisten nicht unterstützt werden, wird " [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) " nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





