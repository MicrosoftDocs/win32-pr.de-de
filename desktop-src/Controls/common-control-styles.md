---
title: Allgemeine Steuerelementstile (CommCtrl.h)
description: In diesem Abschnitt werden allgemeine Steuerelementstile aufgeführt. Sofern nicht anders angegeben, gelten diese Stile für Rebar-Steuerelemente, Symbolleisten-Steuerelemente und Statusfenster.
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
ms.openlocfilehash: bd9ec00cd7cedc4bb105543f932cd5fdcfc76d7c038fb930abb7f0b5d1aeb13d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698820"
---
# <a name="common-control-styles"></a>Allgemeine Steuerelementstile

In diesem Abschnitt werden allgemeine Steuerelementstile aufgeführt. Sofern nicht anders angegeben, gelten diese Stile für Rebar-Steuerelemente, Symbolleisten-Steuerelemente und Statusfenster.



| Konstante                                                                                                                                                                  | Beschreibung                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS \_ ANPASSBAR**</dt> </dl>          | Aktiviert die integrierten Anpassungsfeatures einer Symbolleiste, mit denen der Benutzer eine Schaltfläche an eine neue Position ziehen oder eine Schaltfläche entfernen kann, indem sie von der Symbolleiste gezogen wird. Darüber hinaus kann der Benutzer auf die  Symbolleiste doppelklicken, um das Dialogfeld Symbolleiste anpassen anzuzeigen. Dadurch kann der Benutzer Symbolleistenschaltflächen hinzufügen, löschen und neu anordnen.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS \_ BOTTOM**</dt> </dl>                      | Bewirkt, dass sich das Steuerelement am unteren Rand des Clientbereichs des übergeordneten Fensters positioniert, und legt die Breite auf die gleiche Breite wie das übergeordnete Fenster fest. Statusfenster verfügen standardmäßig über dieses Format.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS \_ LEFT**</dt> </dl>                            | [Version 4.70](common-controls-intro.md). Bewirkt, dass das Steuerelement vertikal auf der linken Seite des übergeordneten Fensters angezeigt wird.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ NODIVIDER**</dt> </dl>             | Verhindert, dass am oberen Ende des Steuerelements eine Hervorhebung mit zwei Pixeln gezeichnet wird. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [Version 4.70](common-controls-intro.md). Bewirkt, dass das Steuerelement die Größe des Steuerelements vertikal, aber nicht horizontal als Reaktion auf eine [**WM \_ SIZE-Meldung geändert und sich selbst bewegt.**](/windows/desktop/winmsg/wm-size) Wenn CCS \_ NORESIZE verwendet wird, gilt dieses Format nicht.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOMOVEY**</dt> </dl>                   | Bewirkt, dass das Steuerelement die Größe des Steuerelements horizontal, aber nicht vertikal als Reaktion auf eine [**WM \_ SIZE-Meldung geändert und sich selbst bewegt.**](/windows/desktop/winmsg/wm-size) Wenn CCS \_ NORESIZE verwendet wird, gilt dieses Format nicht. Headerfenster verfügen standardmäßig über dieses Format.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | Verhindert, dass das Steuerelement automatisch an den anfang oder unteren Rand des übergeordneten Fensters bewegt wird. Stattdessen behält das Steuerelement seine Position im übergeordneten Fenster bei, obwohl sich die Größe des übergeordneten Elements geändert hat. Wenn auch CCS TOP oder CCS BOTTOM verwendet wird, wird die Höhe auf den Standardwert angepasst, die Position \_ und Breite bleiben jedoch \_ unverändert. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | Verhindert, dass das Steuerelement beim Festlegen seiner Anfangsgröße oder einer neuen Größe die Standardbreite und -höhe verwendet. Stattdessen verwendet das Steuerelement die Breite und Höhe, die in der Anforderung für die Erstellung oder Größenerstellung angegeben sind. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS \_ RIGHT**</dt> </dl>                         | [Version 4.70](common-controls-intro.md). Bewirkt, dass das Steuerelement vertikal auf der rechten Seite des übergeordneten Fensters angezeigt wird.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ TOP**</dt> </dl>                               | Bewirkt, dass sich das Steuerelement am oberen Ende des Clientbereichs des übergeordneten Fensters positioniert und die Breite der Breite des übergeordneten Fensters gleicht. Symbolleisten verfügen standardmäßig über diesen Stil. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ VERT**</dt> </dl>                            | [Version 4.70](common-controls-intro.md). Bewirkt, dass das Steuerelement vertikal angezeigt wird.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Hinweise

In den folgenden Themen werden zusätzliche Steuerelementstile beschrieben:

-   [**Animationssteuerstile**](animation-control-styles.md)
-   [**Schaltflächenstile**](button-styles.md)
-   [**Kombinationsfeldstile**](combo-box-styles.md)
-   [**Erweiterte Stile des ComboBoxEx-Steuerelements**](comboboxex-control-extended-styles.md)
-   [**Datums- und Uhrzeitauswahl-Steuerelementstile**](date-and-time-picker-control-styles.md)
-   [**Bearbeiten von Steuerelementstilen**](edit-control-styles.md)
-   [**Header-Steuerelementstile**](header-control-styles.md)
-   [**Listenfeldstile**](list-box-styles.md)
-   [**Fensterstile für Listenansichten**](list-view-window-styles.md)
-   [**Monatskalender-Steuerelementstile**](month-calendar-control-styles.md)
-   [**Pager-Steuerelementstile**](pager-control-styles.md)
-   [**Statusleisten-Steuerelementstile**](progress-bar-control-styles.md)
-   [**Umleisten-Steuerelementstile**](rebar-control-styles.md)
-   [**Rich Edit-Steuerelementstile**](rich-edit-control-styles.md)
-   [**Bildlaufleisten-Steuerelementstile**](scroll-bar-control-styles.md)
-   [Statische Steuerelementstile](static-control-styles.md)
-   [**Statusleistenstile**](status-bar-styles.md)
-   [**SysLink-Steuerelementstile**](syslink-control-styles.md)
-   [**Registerkarten-Steuerelementstile**](tab-control-styles.md)
-   [**Symbolleisten-Steuerelement und Schaltflächenstile**](toolbar-control-and-button-styles.md)
-   [**QuickInfo-Stile**](tooltip-styles.md)
-   [**Trackbar-Steuerelementstile**](trackbar-control-styles.md)
-   [**Fensterstile des Strukturansicht-Steuerelements**](tree-view-control-window-styles.md)
-   [**Auf-Ab-Steuerelementstile**](up-down-control-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

