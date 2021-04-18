---
title: Registerkarten-Steuerelement Stile (kommctrl. h)
description: In diesem Abschnitt werden die unterstützten Registerkarten-Steuerelemente
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352864fe71b5efc39529109bafb3bdc49cee68e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357646"
---
# <a name="tab-control-styles"></a>Register Steuerelement Stile

In diesem Abschnitt werden die unterstützten Registerkarten-Steuerelemente



| Konstante                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TCS \_ unten**</dt> </dl>                                  | [Version 4,70](common-control-versions.md). Registerkarten werden am unteren Rand des Steuer Elements angezeigt. Dieser Wert ist gleich TCS \_ right. Dieser Stil wird nicht unterstützt, wenn Sie ComCtl32.dll Version 6 verwenden.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**TCS- \_ Schaltflächen**</dt> </dl>                               | Registerkarten werden als Schaltflächen angezeigt, und um den Anzeigebereich wird kein Rahmen gezeichnet.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TCS \_ FixedWidth**</dt> </dl>                      | Alle Registerkarten sind identisch. Dieser Stil kann nicht mit dem TCS \_ rightrecht-Stil kombiniert werden.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**TCS- \_ FlatButtons**</dt> </dl>                   | [Version 4,71](common-control-versions.md). Die ausgewählten Registerkarten werden als Einzug in den Hintergrund angezeigt, während andere Registerkarten als auf der gleichen Ebene wie der Hintergrund angezeigt werden. Dieser Stil wirkt sich nur auf Registerkarten-Steuerelemente mit dem TCS- \_ Schaltflächen Stil<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**TCS \_ Focus Never**</dt> </dl>                      | Das Registerkarten-Steuerelement empfängt den Eingabefokus nicht, wenn darauf geklickt wird.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**TCS \_ focusonbuttondown**</dt> </dl> | Das Registerkarten-Steuerelement erhält beim Klicken den Eingabefokus.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**TCS \_ forceienleft**</dt> </dl>             | Symbole werden am linken Rand der einzelnen Registerkarten mit fester Breite ausgerichtet. Dieser Stil kann nur mit dem TCS- \_ FixedWidth-Stil verwendet werden.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**TCS \_ forcelabelleft**</dt> </dl>          | Bezeichnungen werden am linken Rand der einzelnen Registerkarten mit fester Breite ausgerichtet. Das heißt, die Bezeichnung wird direkt rechts neben dem Symbol angezeigt, anstatt zentriert zu werden. Dieser Stil kann nur mit dem TCS \_ -FixedWidth-Stil verwendet werden, und er impliziert das TCS-Format " \_ forceienleft".<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**TCS- \_ HotTrack**</dt> </dl>                            | [Version 4,70](common-control-versions.md). Elemente unter dem Zeiger werden automatisch hervorgehoben. Sie können überprüfen, ob die Hot-Nachverfolgung aktiviert ist, indem Sie [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)aufrufen. <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**mehrzeilige TCS-Funktion \_**</dt> </dl>                         | Bei Bedarf werden mehrere Zeilen mit Registerkarten angezeigt, sodass alle Registerkarten gleichzeitig sichtbar sind.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS- \_ Mehrfachauswahl**</dt> </dl>                   | [Version 4,70](common-control-versions.md). Sie können mehrere Registerkarten auswählen, indem Sie beim Klicken die STRG-Taste gedrückt halten. Dieser Stil muss mit dem TCS-Schaltflächen Stil verwendet werden \_ .<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**TCS- \_ besitzdrawfixed**</dt> </dl>          | Das übergeordnete Fenster ist für das Zeichnen von Registerkarten verantwortlich.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**TCS- \_ raggedright**</dt> </dl>                   | Zeilen von Registerkarten werden nicht gestreckt, um die gesamte Breite des Steuer Elements auszufüllen. Dieser Stil ist die Standardeinstellung.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS- \_ Rechte**</dt> </dl>                                     | [Version 4,70](common-control-versions.md). Registerkarten werden vertikal auf der rechten Seite von Steuerelementen angezeigt, die den vertikalen TCS- \_ Stil verwenden. Dieser Wert ist mit TCS \_ Bottom. Dieses Format wird nicht unterstützt, wenn Sie visuelle Stile verwenden.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**TCS \_ rightrecht**</dt> </dl>                | Die Breite jeder Registerkarte wird bei Bedarf erweitert, sodass jede Zeile von Registerkarten die gesamte Breite des Registerkarten-Steuer Elements füllt. Dieser Fenster Stil wird ignoriert, es sei denn, der \_ mehrzeilige TCS-Stil wird ebenfalls angegeben.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**TCS \_ scrollopposite**</dt> </dl>          | [Version 4,70](common-control-versions.md). Nicht benötigte Registerkarten Scrollen zur gegenüberliegenden Seite des-Steuer Elements, wenn eine Registerkarte ausgewählt wird.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**TCS- \_ SingleLine**</dt> </dl>                      | Es wird nur eine Zeile mit Registerkarten angezeigt. Der Benutzer kann einen Bildlauf durchführen, um ggf. weitere Registerkarten anzuzeigen. Dieser Stil ist die Standardeinstellung.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**TCS- \_ Registerkarten**</dt> </dl>                                        | Registerkarten werden als Registerkarten angezeigt, und es wird ein Rahmen um den Anzeigebereich gezeichnet. Dieser Stil ist die Standardeinstellung.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**TCS- \_ Tooltipps**</dt> </dl>                            | Dem Registerkarten-Steuerelement ist ein QuickInfo-Steuerelement zugeordnet. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ vertikal**</dt> </dl>                            | [Version 4,70](common-control-versions.md). Registerkarten werden auf der linken Seite des-Steuer Elements angezeigt, wobei der Registerkarten Text vertikal angezeigt wird. Dieser Stil ist nur gültig, wenn er mit dem mehrzeiligen TCS-Stil verwendet wird \_ . Verwenden Sie zum Festlegen von Registerkarten auf der rechten Seite des Steuer Elements auch den richtigen TCS- \_ Stil. Dieser Stil wird nicht unterstützt, wenn Sie ComCtl32.dll Version 6 verwenden.<br/> |



## <a name="remarks"></a>Bemerkungen

Die folgenden Stile können geändert werden, nachdem das-Steuerelement erstellt wurde.

-   TCS \_ unten
-   TCS- \_ Schaltflächen
-   TCS \_ FixedWidth
-   TCS- \_ FlatButtons
-   TCS \_ forceienleft
-   TCS \_ forcelabelleft
-   mehrzeilige TCS-Funktion \_
-   TCS- \_ besitzdrawfixed
-   TCS- \_ raggedright
-   TCS- \_ Rechte
-   TCS \_ vertikal

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

