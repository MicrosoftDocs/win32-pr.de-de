---
title: Referenz zu hohen DPI-Daten
description: Referenz zu hohen DPI-Daten
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c10bcf5c5297b0adcfceef6853f2292c3fc8b98
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087798"
---
# <a name="high-dpi-reference"></a>Referenz zu hohen DPI-Daten

## <a name="functions"></a>Functions



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Thema**                                                                                | **Beschreibung**                                                                                                                                                   |
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Eine Variante von [AdjustWindowRectEx,](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) die Werte zurückgibt, die auf einen bestimmten DPI skaliert sind.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Bestimmt, ob [**zwei DPI \_ AWARENESS \_ CONTEXT-Werte**](dpi-awareness-context.md) gleichwertig sind.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Ermöglicht die automatische Skalierung des Nicht-Clientbereichs des angegebenen Fensters der obersten Ebene.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Ruft den [**DPI \_ AWARENESS-Wert**](/windows/desktop/api/windef/ne-windef-dpi_awareness) aus einem [**DPI \_ AWARENESS CONTEXT \_ ab.**](dpi-awareness-context.md)                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Fragt die einem Monitor zugeordneten DPI-Informationen ab.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Gibt den System-DPI zurück.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Gibt den aktuellen DPI-Wert für das angegebene Fenster zurück.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Ruft den DPI-Virtualisierungsmodus des angegebenen Prozesses ab.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Eine Variante von [GetSystemMetrics,](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) die Werte zurückgibt, die auf einen bestimmten DPI skaliert wurden.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Ruft den aktiven DPI-Kontext für den aktuellen Thread ab.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Ruft den DPI-Kontext für ein Fenster ab.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Bestimmt, ob ein [**DPI \_ AWARENESS \_ CONTEXT**](dpi-awareness-context.md) gültig ist und vom aktuellen System unterstützt wird.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Konvertiert einen Punkt in einem Fenster von logischen Koordinaten in physische Koordinaten, unabhängig von der DPI-Kenntnis des Aufrufers.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Konvertiert einen Punkt in einem Fenster von physischen Koordinaten in logische Koordinaten, unabhängig von der DPI-Kenntnis des Aufrufers.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Legt den DPI-Virtualisierungsmodus für den aktuellen Prozess fest.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Ändert den aktiven DPI-Kontext für den aktuellen Thread.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Eine Variante von [SystemParametersInfo,](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) die Werte zurückgibt, die auf einen bestimmten DPI skaliert wurden.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Legt den DPI-Kontext für den aktuellen Prozess fest.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Überschreibt das Standardmäßige DPI-Skalierungsverhalten pro Monitor eines Dialogfelds.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Ruft das DPI-Skalierungsverhalten pro Monitor eines Dialogs ab.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Überschreibt das standardmäßige DPI-Skalierungsverhalten pro Monitor eines untergeordneten Fensters in einem Dialogfeld.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Ruft alle Überschreibungen des DPI-Skalierungsverhaltens pro Monitor eines untergeordneten Fensters in einem Dialogfeld ab.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Eine Variante von [OpenThemeData,](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) die Designhandles öffnet, die einem bestimmten DPI zugeordnet sind. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Ruft den System-DPI ab, der einem bestimmten Prozess zugeordnet ist.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Ruft den DPI aus einem angegebenen [DPI \_ AWARENESS \_ CONTEXT-Handle](dpi-awareness-context.md) ab.                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Überschreibt das DPI-Standardhostingverhalten des aktuellen Threads.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Ruft das DPI-Hostingverhalten des aktuellen Threads ab.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Ruft das DPI-Hostingverhalten des angegebenen Fensters ab.                                                                                                       |



 

## <a name="types"></a>Typen



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Thema**                                                                  | **Beschreibung**                                                                        |
| [**DPI \_ AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Stellt DPI-Koordinatenvirtualisierungsmodi dar.                                        |
| [**\_DPI-KONTEXT \_**](dpi-awareness-context.md)                   | Ein Token, das einen DPI-Virtualisierungsmodus und zugeordnetes Verhalten darstellt.           |
| [**ÄNDERUNGSVERHALTEN VON \_ \_ DIALOGSTEUERELEMENT-DPI \_ \_**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Beschreibt Überschreibungen des DPI-Skalierungsverhaltens pro Monitor für untergeordnete Fenster in Dialogen. |
| [**\_ \_ DIALOG-DPI-ÄNDERUNGSVERHALTEN \_**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Beschreibt Überschreibungen des DPI-Skalierungsverhaltens pro Monitor für Dialoge.                      |
| [**\_ \_ MONITOR-DPI-TYP**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Stellt den DPI-Typ dar, der einem Monitor zugeordnet ist.                                  |
| [**\_ \_ PROZESS-DPI-KENNTNIS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Stellt den DPI-Koordinatenvirtualisierungsmodus eines Prozesses dar.                        |
| [**\_DPI-HOSTINGVERHALTEN \_**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Stellt das DPI-Hostingverhalten für ein Fenster dar.                                      |



 

## <a name="messages"></a>Meldungen



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Thema**                                                          | **Beschreibung**                                                                                                                         |
| [**WM \_ DPICHANGED**](wm-dpichanged.md)                            | Benachrichtigt ein Fenster der obersten Ebene, dass sich der DPI geändert hat.                                                                                   |
| [**WM \_ DPICHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md) | Benachrichtigt ein untergeordnetes Fenster, dass sich der dem enthaltenden Fenster zugeordnete DPI geändert hat. Wird übermittelt, bevor das übergeordnete Fenster benachrichtigt wird. |
| [**WM \_ DPICHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)   | Benachrichtigt ein untergeordnetes Fenster, dass sich der dem enthaltenden Fenster zugeordnete DPI geändert hat. Wird übermittelt, nachdem das übergeordnete Fenster benachrichtigt wurde.  |
| [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md)                | Ermöglicht es Fenstern der obersten Ebene, die Größe nicht linear als Reaktion auf *DPI-Änderungen* zu ändern.                                                           |



 

 

 
