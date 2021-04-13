---
title: Hoher dpi-Verweis
description: .
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec59f34aa5ed036d7f4376cb3d170b5d7849f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390164"
---
# <a name="high-dpi-reference"></a>Hoher dpi-Verweis

## <a name="functions"></a>Functions



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Thema**                                                                                | **Beschreibung**                                                                                                                                                   |
| [**"Setting windowrectexfordpi"**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Eine Variante von "Setting [windowrectex](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) ", die auf einen bestimmten dpi-Wert skalierte Werte zurückgibt.       |
| [**Aredpiawareness contextsequal**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Bestimmt, ob zwei [**dpi- \_ \_ Kontext**](dpi-awareness-context.md) Werte äquivalent sind.                                                            |
| [**Enablenonclientdpiscalung**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Aktiviert die automatische Skalierung des nicht-Client Bereichs des angegebenen Fensters der obersten Ebene.                                                                               |
| [**Getawarenmefromdpiawarretecontext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Ruft den [**dpi- \_ Bekanntheits**](/windows/desktop/api/windef/ne-windef-dpi_awareness) Wert aus einem [**dpi-Awareness- \_ \_ Kontext**](dpi-awareness-context.md) ab.                                       |
| [**Getdpiformonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Fragt die einem Monitor zugeordneten dpi-Informationen ab.                                                                                                            |
| [**Getdpiforsystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Gibt das System-dpi zurück.                                                                                                                                           |
| [**Getdpiforwindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Gibt den aktuellen dpi-Wert für das angegebene Fenster zurück.                                                                                                                 |
| [**Getprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Ruft den dpi-Virtualisierungsmodus des angegebenen Prozesses ab.                                                                                                   |
| [**Getsystemmetricsfordpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Eine Variante von [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , die auf einen bestimmten dpi-Wert skalierte Werte zurückgibt.         |
| [**Getthreaddpiawareress Context**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Ruft den aktiven dpi-Kontext für den aktuellen Thread ab.                                                                                                |
| [**Getwindowdpiawareress Context**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Ruft den dpi-kontextkontext für ein Fenster ab.                                                                                                                 |
| [**Isvaliddpiawareress Context**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Bestimmt, ob ein [**dpi- \_ \_ Kontext**](dpi-awareness-context.md) gültig ist und vom aktuellen System unterstützt wird.                                            |
| [**Logicaltophysicalpointforpermonitordpi**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Konvertiert einen Punkt in einem Fenster von logischen Koordinaten in physische Koordinaten, unabhängig von der dpi-Bekanntheit des Aufrufers.                                   |
| [**Physicaltologicalpointforpermonitordpi**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Konvertiert einen Punkt in einem Fenster von physischen Koordinaten in logische Koordinaten, unabhängig von der dpi-Bekanntheit des Aufrufers.                                   |
| [**Setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Legt den dpi-Virtualisierungsmodus für den aktuellen Prozess fest.                                                                                                         |
| [**Setthreaddpiawareress Context**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Ändert den aktiven dpi-Awareness-Kontext für den aktuellen Thread.                                                                                                  |
| [**Systemparametersinfofordpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Eine Variante von [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) , die Werte zurückgibt, die auf einen bestimmten dpi skaliert werden.     |
| [**Setprocessdpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Legt den Kontext des dpi-Kontexts für den aktuellen Prozess fest.                                                                                                           |
| [**Setdialodspichangebehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Überschreibt das standardmäßige dpi-Skalierungs Verhalten eines Dialogs pro Monitor.                                                                                               |
| [**Getdialodspichangebehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Ruft das dpi-Skalierungs Verhalten pro Monitor eines Dialogs ab.                                                                                                       |
| [**Setdialogcontroldpichangebehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Überschreibt das standardmäßige dpi-Skalierungs Verhalten pro Monitor eines untergeordneten Fensters in einem Dialogfeld.                                                                             |
| [**Getdialogcontroldpichangebehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Ruft eine beliebige Monitor übergreifende dpi-Skalierungs Verhaltens Überschreibungen eines untergeordneten Fensters in einem Dialogfeld ab.                                                                           |
| [**Openfomedatafordpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Eine Variante von [opendermedata](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) , die Design Handles öffnet, die einem bestimmten dpi zugeordnet sind. |
| [**Getsystemdpiforprocess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Ruft das System-dpi ab, das einem bestimmten Prozess zugeordnet ist.                                                                                                         |
| [**Getdpifromdpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Ruft das dpi von einem angegebenen [Kontext Handle für den dpi- \_ \_ Kontext](dpi-awareness-context.md) ab.                                                                       |
| [**Setthreaddpihostingbehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Überschreibt das standardmäßige dpi-hostingverhalten des aktuellen Threads.                                                                                                 |
| [**Getthreaddpihostingbehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Ruft das dpi-hostingverhalten des aktuellen Threads ab.                                                                                                         |
| [**Getwindowdpihostingbehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Ruft das dpi-hostingverhalten des angegebenen Fensters ab.                                                                                                       |



 

## <a name="types"></a>Typen



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Thema**                                                                  | **Beschreibung**                                                                        |
| [**DPI \_ -Informationen**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Stellt dpi-koordinatenvirtualisierungsmodi dar.                                        |
| [**\_Kontext für dpi-Informationen \_**](dpi-awareness-context.md)                   | Ein Token, das einen dpi-Virtualisierungsmodus und zugehörige Verhalten darstellt.           |
| [**Dialog Feld \_ Steuerung \_ dpi- \_ Änderungs \_ Verhalten**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Beschreibt die über schreibungen der dpi-Skalierungs Verhalten pro Monitor für untergeordnete Fenster in Dialogfeldern. |
| [**Dialog Feld \_ dpi- \_ Änderungs \_ Verhalten**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Beschreibt die über schreibungen der dpi-Skalierungs Verhalten pro Monitor für Dialoge.                      |
| [**\_dpi- \_ Typ überwachen**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Stellt den einem Monitor zugeordneten dpi-Typ dar.                                  |
| [**Prozess- \_ dpi- \_ Bewusstsein**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Stellt den dpi-koordinatenvirtualisierungsmodus eines Prozesses dar.                        |
| [**DPI \_ - \_ hostingverhalten**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Stellt das dpi-hostingverhalten für ein Fenster dar.                                      |



 

## <a name="messages"></a>Meldungen



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Thema**                                                          | **Beschreibung**                                                                                                                         |
| [**WM- \_ dpichanged**](wm-dpichanged.md)                            | Benachrichtigt ein Fenster auf oberster Ebene, dass sich der dpi-Wert geändert hat.                                                                                   |
| [**WM \_ dpichanged \_ beforeparent**](wm-dpichanged-beforeparent.md) | Benachrichtigt ein untergeordnetes Fenster, dass sich der dem enthaltenden Fenster zugeordnete dpi-Wert geändert hat. Übermittelt, bevor das übergeordnete Fenster benachrichtigt wird. |
| [**WM- \_ dpichanged nach dem über \_ geordneten Element**](wm-dpichanged-afterparent.md)   | Benachrichtigt ein untergeordnetes Fenster, dass sich der dem enthaltenden Fenster zugeordnete dpi-Wert geändert hat. Wird zugestellt, nachdem das übergeordnete Fenster benachrichtigt wurde.  |
| [**WM \_ getdpiscaledsize**](wm-getdpiscaledsize.md)                | Ermöglicht es Fenstern der obersten Ebene, die Größe *nicht linear* in Reaktion auf dpi-Änderungen zu ändern.                                                           |



 

 

 