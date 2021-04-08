---
title: Andere Objekt Rollen und unterstützte Methoden (MSAA UI-Element Referenz)
description: Dieses Thema enthält Informationen zu Objekt Rollen, die nicht in den vorherigen Themen zu Benutzeroberflächen Elementen enthalten sind.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729025"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Andere Objekt Rollen und unterstützte Methoden (MSAA UI-Element Referenz)

Dieses Thema enthält Informationen zu Objekt Rollen, die nicht in den vorherigen Themen zu Benutzeroberflächen Elementen enthalten sind. Jede Objekt Rolle enthält eine Liste der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden und-Eigenschaften, die für die Objekt Rolle unterstützt werden. In anderen Themen werden unterstützte **IAccessible** -Methoden und-Eigenschaften für Benutzeroberflächen Elemente dokumentiert. in diesem Thema werden die Methoden und Eigenschaften aufgelistet, die für eine bestimmte Objekt Rolle erwartet werden. Viele Benutzeroberflächen Elemente, die möglicherweise eine der hier aufgeführten Rollen aufweisen, werden in der Regel in Browsern angezeigt.

> [!Note]  
> Verwenden Sie dieses Thema als Richtlinie. Wir empfehlen dringend, Microsoft Active Accessibility Tools zu verwenden, um das erwartete Verhalten für eine einzelne Objekt Rolle zu überprüfen.

 

In der folgenden Tabelle werden zusätzliche Objekt Rollen aufgelistet, die Oleacc.dll unterstützt.



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Rollen \_ System \_ Warnung**](/windows)                           | [**Rollen \_ System- \_ Dropdown Liste**](/windows)       |
| [**Rollen \_ System \_ Anwendung**](/windows)               | [**Rollen \_ System \_ Gleichung**](/windows)       |
| [**Rollen \_ System \_ Rahmen**](/windows)                         | [**Grafik zum Rollen \_ System \_**](/windows)         |
| [**\_ \_ ButtonDropDown für Rollen System**](/windows)         | [**Hilfe Sprechblase für Rollen \_ System \_**](/windows) |
| [**\_ \_ buttondropdowngrid für Rollen System**](/windows) | [**Rollen \_ System- \_ IPAddress**](/windows)     |
| [**\_ \_ ButtonMenu für Rollen System**](/windows)                 | [**Rollen \_ System \_ Link**](/windows)               |
| [**Rollen \_ System \_ Zelle**](/windows)                             | [**Bereich "Rollen \_ System" \_**](/windows)               |
| [**Rollen \_ System \_ Zeichen**](/windows)                   | [**Rollen \_ System \_ Zeile**](/windows)                 |
| [**Rollen \_ System \_ Diagramm**](/windows)                           | [**Rollen \_ System ( \_ RowHeader)**](/windows)     |
| [**Rollen \_ \_ Systemuhr**](/windows)                           | [**Rollen \_ System \_ Trennzeichen**](/windows)     |
| [**Rollen \_ System \_ Spalte**](/windows)                         | [**Sound des Rollen \_ Systems \_**](/windows)             |
| [**Rollen \_ System \_ Diagramm**](/windows)                       | [**Rollen \_ System ( \_ SplitButton)**](/windows) |
| [**Rollen \_ System- \_ Wahl**](/windows)                             | [**Rollen \_ System \_ Tabelle**](/windows)             |
| [**Rollen \_ System \_ Dokument**](/windows)                     | [**\_Leerraum für Rollen System \_**](/windows)   |



 

## <a name="role_system_alert"></a>Rollen \_ System \_ Warnung

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Warnung zu Rollen Systemen**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   \_accName erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_application"></a>Rollen \_ System \_ Anwendung

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Application**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_border"></a>Rollen \_ System \_ Rahmen

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Border**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_buttondropdown"></a>\_ \_ ButtonDropDown für Rollen System

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ ButtonDropDown für Rollen System**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   get \_ accdefaultaction
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_buttondropdowngrid"></a>\_ \_ buttondropdowngrid für Rollen System

Weitere Informationen zu dieser Rolle finden Sie im Thema zum [**Rollen \_ System \_ buttondropdowngrid**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   get \_ accdefaultaction
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_buttonmenu"></a>\_ \_ ButtonMenu für Rollen System

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ Button- \_ Menü "Rollen System**](object-roles.md)".

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accdefaultaction
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_cell"></a>Rollen \_ System \_ Zelle

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Cell**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_character"></a>Rollen \_ System \_ Zeichen

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Character**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   get- \_ accdescription
-   \_Zugriffs Fokus erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_chart"></a>Rollen \_ System \_ Diagramm

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Chart**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_clock"></a>Rollen \_ \_ Systemuhr

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Clock**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_column"></a>Rollen \_ System \_ Spalte

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Column**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_diagram"></a>Rollen \_ System \_ Diagramm

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Diagram**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_dial"></a>Rollen \_ System- \_ Wahl

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Dial**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accdefaultaction
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_document"></a>Rollen \_ System \_ Dokument

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Document**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_droplist"></a>Rollen \_ System- \_ Dropdown Liste

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ droplist**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   get \_ accdefaultaction
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_equation"></a>Rollen \_ System \_ Gleichung

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Gleichung**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_Zugriffs Fokus erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_graphic"></a>Grafik zum Rollen \_ System \_

Weitere Informationen zu dieser Rolle finden Sie in [**der \_ \_ Grafik zum Rollen System**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_helpballoon"></a>Hilfe Sprechblase für Rollen \_ System \_

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ helpballoon für Rollen Systeme**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   get \_ accdefaultaction
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_ipaddress"></a>Rollen \_ System- \_ IPAddress

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ IPAddress**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_link"></a>Rollen \_ System \_ Link

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Link**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   get \_ accdefaultaction
-   get- \_ accdescription
-   \_Zugriffs Fokus erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_pane"></a>Bereich "Rollen \_ System" \_

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Pane**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   \_accChild erhalten
-   get \_ accChildCount
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_row"></a>Rollen \_ System \_ Zeile

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Row**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   \_accChild erhalten
-   get \_ accChildCount
-   get- \_ accdescription
-   \_Zugriffs Fokus erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_rowheader"></a>Rollen \_ System ( \_ RowHeader)

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ RowHeader**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   \_accChild erhalten
-   get \_ accChildCount
-   get \_ accdefaultaction
-   get- \_ accdescription
-   \_Zugriffs Fokus erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten
-   \_accValue erhalten

## <a name="role_system_separator"></a>Rollen \_ System \_ Trennzeichen

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Trennzeichen für Rollen Systeme**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   \_accChild erhalten
-   get \_ accChildCount
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_sound"></a>Sound des Rollen \_ Systems \_

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Sound des Rollen Systems**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   get- \_ accdescription
-   \_accName erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_splitbutton"></a>Rollen \_ System ( \_ SplitButton)

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ SplitButton**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accdefaultaction
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_table"></a>Rollen \_ System \_ Tabelle

Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Table**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   \_accChild erhalten
-   get \_ accChildCount
-   get- \_ accdescription
-   \_Zugriffs Fokus erhalten
-   \_accHelp erhalten
-   \_accHelpTopic erhalten
-   \_accKeyboardShortcut erhalten
-   \_accName erhalten
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

## <a name="role_system_whitespace"></a>\_Leerraum für Rollen System \_

Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Leerraum für Rollen Systeme**](object-roles.md).

**Unterstützte Eigenschaften und Methoden**

-   accLocation
-   accSelect
-   \_accParent erhalten
-   get- \_ Zugriffs Rolle
-   \_accState erhalten

 

 