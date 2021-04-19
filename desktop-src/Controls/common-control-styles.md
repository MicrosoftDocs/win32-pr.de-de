---
title: Allgemeine Steuerelement Stile (kommctrl. h)
description: In diesem Abschnitt werden allgemeine Steuerelement Stile aufgeführt. Sofern nicht angegeben, gelten diese Stile für Grund leisten-Steuerelemente, Symbolleisten-Steuerelemente und Statusfenster.
ms.assetid: aab0cd68-ede7-474b-8695-c75805669716
topic_type:
- apiref
api_name:
- CCS_ADJUSTABLE
- CCS_BOTTOM
- CCS_LEFT
- CCS_NODIVIDER
- CCS_NOMOVEX
- CCS_NOMOVEY
- CCS_NOPARENTALIGN
- CCS_NORESIZE
- CCS_RIGHT
- CCS_TOP
- CCS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a50b28a95d94a97da2fb6ac3522dbc568af111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372362"
---
# <a name="common-control-styles"></a>Allgemeine Steuerelement Stile

In diesem Abschnitt werden allgemeine Steuerelement Stile aufgeführt. Sofern nicht angegeben, gelten diese Stile für Grund leisten-Steuerelemente, Symbolleisten-Steuerelemente und Statusfenster.



| Konstante                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS- \_ anpassbar**</dt> </dl>          | Aktiviert die integrierten Anpassungs Features einer Symbolleiste, die es dem Benutzer ermöglichen, eine Schaltfläche an eine neue Position zu ziehen oder eine Schaltfläche zu entfernen, indem Sie Sie aus der Symbolleiste ziehen. Außerdem kann der Benutzer auf die Symbolleiste doppelklicken, um das Dialogfeld **Symbolleiste anpassen** anzuzeigen, in dem der Benutzer Symbolleisten Schaltflächen hinzufügen, löschen und neu anordnen kann.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS \_ unten**</dt> </dl>                      | Bewirkt, dass sich das Steuerelement am unteren Rand des Client Bereichs des übergeordneten Fensters positioniert und die Breite auf die Breite des übergeordneten Fensters festgelegt wird. Status Fenster haben dieses Format standardmäßig.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS \_ Links**</dt> </dl>                            | [Version 4,70](common-controls-intro.md). Bewirkt, dass das Steuerelement auf der linken Seite des übergeordneten Fensters vertikal angezeigt wird.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS- \_ nodivider**</dt> </dl>             | Verhindert, dass eine zwei-Pixel-Hervorhebung am oberen Rand des-Steuer Elements gezeichnet wird. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ nomovex**</dt> </dl>                   | [Version 4,70](common-controls-intro.md). Bewirkt, dass die Größe des Steuer Elements in Reaktion auf eine [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht vertikal, aber nicht horizontal geändert wird. Wenn CCS \_ NORESIZE verwendet wird, gilt dieser Stil nicht.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ nomovey**</dt> </dl>                   | Bewirkt, dass die Größe des Steuer Elements in Reaktion auf eine [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht horizontal, aber nicht vertikal geändert wird. Wenn CCS \_ NORESIZE verwendet wird, gilt dieser Stil nicht. Header Fenster haben diesen Stil standardmäßig.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ noparentalign**</dt> </dl> | Verhindert, dass das-Steuerelement automatisch an den oberen oder unteren Rand des übergeordneten Fensters wechselt. Stattdessen behält das Steuerelement seine Position innerhalb des übergeordneten Fensters, trotz der Änderungen an der Größe des übergeordneten Fensters. Wenn CCS \_ Top oder CCS \_ Bottom ebenfalls verwendet wird, wird die Höhe auf den Standardwert angepasst, die Position und Breite bleiben jedoch unverändert. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | Verhindert, dass das Steuerelement beim Festlegen der Anfangs Größe oder einer neuen Größe die Standardbreite und-Höhe verwendet. Stattdessen verwendet das Steuerelement die Breite und die Höhe, die in der Anforderung für die Erstellung oder Größenanpassung angegeben sind. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS ( \_ rechts)**</dt> </dl>                         | [Version 4,70](common-controls-intro.md). Bewirkt, dass das Steuerelement auf der rechten Seite des übergeordneten Fensters vertikal angezeigt wird.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS ( \_ oben)**</dt> </dl>                               | Bewirkt, dass das Steuerelement sich selbst am oberen Rand des Client Bereichs des übergeordneten Fensters positioniert und die Breite auf die Breite der übergeordneten Fensterbreite festgelegt wird. Symbolleisten haben diesen Stil standardmäßig. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS- \_ Vert**</dt> </dl>                            | [Version 4,70](common-controls-intro.md). Bewirkt, dass das Steuerelement vertikal angezeigt wird.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Bemerkungen

In den folgenden Themen werden zusätzliche Steuerelement Stile beschrieben:

-   [**Animations Steuerelement Stile**](animation-control-styles.md)
-   [**Schaltflächen Stile**](button-styles.md)
-   [**Kombinations Feld Stile**](combo-box-styles.md)
-   [**Erweiterte Stile des ComboBoxEx-Steuer Elements**](comboboxex-control-extended-styles.md)
-   [**Steuerelement Stile für Datums-und Zeitauswahl**](date-and-time-picker-control-styles.md)
-   [**Steuerelement Stile bearbeiten**](edit-control-styles.md)
-   [**Header Steuerelement Stile**](header-control-styles.md)
-   [**Listenfeld Stile**](list-box-styles.md)
-   [**Fenster Stile für Listenansicht**](list-view-window-styles.md)
-   [**Monatskalender-Steuerelement Stile**](month-calendar-control-styles.md)
-   [**Pager-Steuerelement Stile**](pager-control-styles.md)
-   [**Stile der Statusanzeige-Steuerelemente**](progress-bar-control-styles.md)
-   [**Grund leisten-Steuerelement Stile**](rebar-control-styles.md)
-   [**Rich Edit-Steuerelement Stile**](rich-edit-control-styles.md)
-   [**ScrollBar-Steuerelement Stile**](scroll-bar-control-styles.md)
-   [Statische Steuerelement Stile](static-control-styles.md)
-   [**StatusBar-Stile**](status-bar-styles.md)
-   [**Syslink-Steuerelement Stile**](syslink-control-styles.md)
-   [**Register Steuerelement Stile**](tab-control-styles.md)
-   [**ToolBar-Steuerelement und Schaltflächen Stile**](toolbar-control-and-button-styles.md)
-   [**QuickInfo-Stile**](tooltip-styles.md)
-   [**TrackBar-Steuerelement Stile**](trackbar-control-styles.md)
-   [**Fenster Stile des Strukturansicht-Steuer Elements**](tree-view-control-window-styles.md)
-   [**Auf-ab-Steuerelement Stile**](up-down-control-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

