---
title: Andere Objektrollen und unterstützte Methoden (REFERENZ ZUM MSAA-UI-Element)
description: Dieses Thema enthält Informationen zu Objektrollen, die in den vorherigen Themen für Benutzeroberflächenelemente nicht enthalten sind.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444001"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Andere Objektrollen und unterstützte Methoden (REFERENZ ZUM MSAA-UI-Element)

Dieses Thema enthält Informationen zu Objektrollen, die in den vorherigen Themen für Benutzeroberflächenelemente nicht enthalten sind. Jede Objektrolle enthält eine Liste der [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Eigenschaften, die für die Objektrolle unterstützt werden. Während in anderen Themen unterstützte **IAccessible-Methoden** und -Eigenschaften für Benutzeroberflächenelemente dokumentiert sind, werden in diesem Thema die Methoden und Eigenschaften aufgeführt, die für eine bestimmte Objektrolle unterstützt werden sollen. Viele der Benutzeroberflächenelemente, die möglicherweise über eine der hier aufgeführten Rollen verfügen, werden in der Regel in Browsern angezeigt.

> [!Note]  
> Verwenden Sie dieses Thema als Richtlinie. Es wird dringend empfohlen, Microsoft Active Accessibility Tools zu verwenden, um das erwartete Verhalten für eine einzelne Objektrolle zu überprüfen.

 

In der folgenden Tabelle sind zusätzliche Objektrollen aufgeführt, die Oleacc.dll unterstützen.



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ROLE \_ SYSTEM \_ ALERT**](/windows)                           | [**ROLE \_ SYSTEM \_ DROPLIST**](/windows)       |
| [**\_ \_ ROLLENSYSTEMANWENDUNG**](/windows)               | [**\_ \_ ROLLENSYSTEMGLEICHUNG**](/windows)       |
| [**ROLE \_ SYSTEM \_ BORDER**](/windows)                         | [**\_ \_ ROLLENSYSTEMGRAFIK**](/windows)         |
| [**\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWN**](/windows)         | [**ROLE \_ SYSTEM \_ HELPBALLOON**](/windows) |
| [**\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWNGRID**](/windows) | [**\_ \_ ROLLENSYSTEM-IPADDRESS**](/windows)     |
| [**SCHALTFLÄCHE \_ \_ "ROLLENSYSTEM"MENU**](/windows)                 | [**ROLE \_ SYSTEM \_ LINK**](/windows)               |
| [**\_ \_ ROLLENSYSTEMZELLE**](/windows)                             | [**BEREICH \_ \_ "ROLLENSYSTEM"**](/windows)               |
| [**\_ \_ ROLLENSYSTEMZEICHEN**](/windows)                   | [**ROLE \_ SYSTEM \_ ROW**](/windows)                 |
| [**\_ \_ ROLLENSYSTEMDIAGRAMM**](/windows)                           | [**ROLE \_ SYSTEM \_ ROWHEADER**](/windows)     |
| [**ROLE \_ SYSTEM \_ CLOCK**](/windows)                           | [**\_ \_ ROLLENSYSTEMTRENNZEICHEN**](/windows)     |
| [**ROLE \_ SYSTEM \_ COLUMN**](/windows)                         | [**ROLE \_ SYSTEM \_ SOUND**](/windows)             |
| [**\_ \_ ROLLENSYSTEMDIAGRAMM**](/windows)                       | [**\_ \_ ROLLENSYSTEM-SPLITBUTTON**](/windows) |
| [**\_ \_ ROLLENSYSTEMWAHL**](/windows)                             | [**ROLE \_ SYSTEM \_ TABLE**](/windows)             |
| [**ROLE \_ SYSTEM DOCUMENT (ROLLENSYSTEMDOKUMENT) \_**](/windows)                     | [**\_ \_ ROLLENSYSTEM-LEERRAUM**](/windows)   |



 

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

## <a name="role_system_border"></a>ROLE \_ SYSTEM \_ BORDER

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BORDER**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdown"></a>\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWN

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

## <a name="role_system_buttondropdowngrid"></a>\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWNGRID

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

## <a name="role_system_buttonmenu"></a>SCHALTFLÄCHE \_ \_ "ROLLENSYSTEM"MENU

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

## <a name="role_system_cell"></a>\_ \_ ROLLENSYSTEMZELLE

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

Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DIAGRAM**](object-roles.md).

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

## <a name="role_system_dial"></a>\_ \_ ROLLENSYSTEMWAHL

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

## <a name="role_system_document"></a>ROLE \_ SYSTEM DOCUMENT (ROLLENSYSTEMDOKUMENT) \_

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

## <a name="role_system_graphic"></a>\_ \_ ROLLENSYSTEMGRAFIK

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

## <a name="role_system_ipaddress"></a>ROLE \_ SYSTEM \_ IPADDRESS

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

## <a name="role_system_pane"></a>\_BEREICH \_ "ROLLENSYSTEM"

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

 

 