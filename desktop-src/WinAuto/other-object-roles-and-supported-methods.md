---
title: Andere Objektrollen und unterstützte Methoden (MSAA UI-Elementreferenz)
description: Dieses Thema enthält Informationen zu Objektrollen, die in den vorherigen Themen für Benutzeroberflächenelemente nicht enthalten sind.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e29a4ef0345513912c8ad08e3a322e01b56bd3245291e9def64a49b35ac22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052568"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Andere Objektrollen und unterstützte Methoden (MSAA UI-Elementreferenz)

Dieses Thema enthält Informationen zu Objektrollen, die in den vorherigen Themen für Benutzeroberflächenelemente nicht enthalten sind. Jede Objektrolle enthält eine Liste der [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Eigenschaften, die für die Objektrolle unterstützt werden. Während in anderen Themen unterstützte **IAccessible-Methoden** und -Eigenschaften für Benutzeroberflächenelemente dokumentiert werden, werden in diesem Thema die Methoden und Eigenschaften aufgelistet, die für eine bestimmte Objektrolle unterstützt werden können. Viele der Benutzeroberflächenelemente, die möglicherweise über eine der hier aufgeführten Rollen verfügen, werden in der Regel in Browsern angezeigt.

> [!Note]  
> Verwenden Sie dieses Thema als Richtlinie. Es wird dringend empfohlen, Microsoft Active Accessibility Tools zu verwenden, um das erwartete Verhalten für eine einzelne Objektrolle zu überprüfen.

 

In der folgenden Tabelle sind zusätzliche Objektrollen aufgeführt, die Oleacc.dll unterstützt.



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ROLE \_ SYSTEM \_ ALERT**](/windows)                           | [**ROLE \_ SYSTEM \_ DROPLIST**](/windows)       |
| [**\_ \_ ROLLENSYSTEMANWENDUNG**](/windows)               | [**\_ \_ ROLLENSYSTEMGLEICHUNG**](/windows)       |
| [**RAHMEN \_ DES ROLLENSYSTEMS \_**](/windows)                         | [**\_GRAFIK ZUM ROLLENSYSTEM \_**](/windows)         |
| [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](/windows)         | [**ROLE \_ SYSTEM \_ HELPBALLOON**](/windows) |
| [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](/windows) | [**ROLE \_ SYSTEM \_ IPADDRESS**](/windows)     |
| [**ROLE \_ SYSTEM \_ BUTTONMENU**](/windows)                 | [**ROLE \_ SYSTEM \_ LINK**](/windows)               |
| [**ROLE \_ SYSTEM \_ CELL**](/windows)                             | [**\_BEREICH \_ "ROLLENSYSTEM"**](/windows)               |
| [**\_ \_ ROLLENSYSTEMZEICHEN**](/windows)                   | [**ROLE \_ SYSTEM \_ ROW**](/windows)                 |
| [**\_ \_ ROLLENSYSTEMDIAGRAMM**](/windows)                           | [**ROLE \_ SYSTEM \_ ROWHEADER**](/windows)     |
| [**ROLE \_ SYSTEM \_ CLOCK**](/windows)                           | [**\_ \_ ROLLENSYSTEMTRENNZEICHEN**](/windows)     |
| [**ROLE \_ SYSTEM \_ COLUMN**](/windows)                         | [**ROLE \_ SYSTEM \_ SOUND**](/windows)             |
| [**\_ \_ ROLLENSYSTEMDIAGRAMM**](/windows)                       | [**ROLE \_ SYSTEM \_ SPLITBUTTON**](/windows) |
| [**\_ \_ ROLLENSYSTEMWÄHL**](/windows)                             | [**ROLE \_ SYSTEM \_ TABLE**](/windows)             |
| [**\_ \_ ROLLENSYSTEMDOKUMENT**](/windows)                     | [**LEERRAUM \_ DES ROLLENSYSTEMS \_**](/windows)   |



 

## <a name="role_system_alert"></a>ROLE \_ SYSTEM \_ ALERT

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ ALERT**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   get \_ accName
-   get \_ accRole
-   get \_ accState

## <a name="role_system_application"></a>\_ \_ ROLLENSYSTEMANWENDUNG

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ APPLICATION**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_border"></a>RAHMEN \_ DES ROLLENSYSTEMS \_

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BORDER**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdown"></a>ROLE \_ SYSTEM \_ BUTTONDROPDOWN

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdowngrid"></a>ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttonmenu"></a>ROLE \_ SYSTEM \_ BUTTONMENU

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_cell"></a>ROLE \_ SYSTEM \_ CELL

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_character"></a>\_ \_ ROLLENSYSTEMZEICHEN

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_chart"></a>\_ \_ ROLLENSYSTEMDIAGRAMM

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CHART**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_clock"></a>ROLE \_ SYSTEM \_ CLOCK

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_column"></a>ROLE \_ SYSTEM \_ COLUMN

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ COLUMN**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_diagram"></a>\_ \_ ROLLENSYSTEMDIAGRAMM

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ ROLLENSYSTEMDIAGRAMM.**](object-roles.md)

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_dial"></a>\_ \_ ROLLENSYSTEMWÄHL

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DIAL**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_document"></a>\_ \_ ROLLENSYSTEMDOKUMENT

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_droplist"></a>ROLE \_ SYSTEM \_ DROPLIST

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_equation"></a>\_ \_ ROLLENSYSTEMGLEICHUNG

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_graphic"></a>\_GRAFIK ZUM ROLLENSYSTEM \_

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_helpballoon"></a>ROLE \_ SYSTEM \_ HELPBALLOON

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ HELPBALLOON**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_ipaddress"></a>\_ \_ ROLLENSYSTEM-IPADDRESS

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_link"></a>ROLE \_ SYSTEM \_ LINK

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_pane"></a>BEREICH \_ \_ "ROLLENSYSTEM"

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ PANE**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_row"></a>ROLE \_ SYSTEM \_ ROW

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_rowheader"></a>ROLE \_ SYSTEM \_ ROWHEADER

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_separator"></a>\_ \_ ROLLENSYSTEMTRENNZEICHEN

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_sound"></a>ROLE \_ SYSTEM \_ SOUND

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   get \_ accDescription
-   get \_ accName
-   get \_ accRole
-   get \_ accState

## <a name="role_system_splitbutton"></a>\_ \_ ROLLENSYSTEM-SPLITBUTTON

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_table"></a>ROLE \_ SYSTEM \_ TABLE

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ TABLE**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_whitespace"></a>\_ \_ ROLLENSYSTEM-LEERRAUM

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ WHITESPACE**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accLocation
-   accSelect
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

 

 