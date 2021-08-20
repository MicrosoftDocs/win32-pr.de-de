---
title: Registerkarten-Steuerelementstile (CommCtrl.h)
description: In diesem Abschnitt werden unterstützte Stile für Registerkartensteuerelement aufgelistet.
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
ms.openlocfilehash: ec4dfdcfb17b2f4a8ffebd4a7cfba5042e19ba2b566d4b03635032438a2f7fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078414"
---
# <a name="tab-control-styles"></a>Stile des Registerkartensteuerelements

In diesem Abschnitt werden unterstützte Stile für Registerkartensteuerelement aufgelistet.



| Konstante                                                                                                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TCS \_ BOTTOM**</dt> </dl>                                  | [Version 4.70.](common-control-versions.md) Am unteren Rand des Steuerelements werden Registerkarten angezeigt. Dieser Wert entspricht TCS \_ RIGHT. Dieser Stil wird nicht unterstützt, wenn Sie ComCtl32.dll Version 6 verwenden.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**\_TCS-SCHALTFLÄCHEN**</dt> </dl>                               | Registerkarten werden als Schaltflächen angezeigt, und um den Anzeigebereich wird kein Rahmen gezeichnet.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TCS \_ FIXEDWIDTH**</dt> </dl>                      | Alle Registerkarten haben die gleiche Breite. Dieser Stil kann nicht mit dem TCS \_ RIGHTJUSTIFY-Stil kombiniert werden.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**TCS \_ FLATBUTTONS**</dt> </dl>                   | [Version 4.71.](common-control-versions.md) Ausgewählte Registerkarten werden als eingerückt im Hintergrund angezeigt, während andere Registerkarten auf der gleichen Ebene wie der Hintergrund angezeigt werden. Dieser Stil wirkt sich nur auf Registerkartensteuerelemente mit dem TCS \_ BUTTONS-Stil aus.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**TCS \_ FOCUSNEVER**</dt> </dl>                      | Das Registerkartensteuerelement erhält nicht den Eingabefokus, wenn darauf geklickt wird.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**TCS \_ FOCUSONBUTTONDOWN**</dt> </dl> | Das Registerkartensteuerelement empfängt den Eingabefokus, wenn darauf geklickt wird.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**TCS \_ FORCEICONLEFT**</dt> </dl>             | Symbole werden am linken Rand jeder Registerkarte mit fester Breite ausgerichtet. Dieser Stil kann nur mit dem TCS \_ FIXEDWIDTH-Stil verwendet werden.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**TCS \_ FORCELABELLEFT**</dt> </dl>          | Bezeichnungen werden am linken Rand jeder Registerkarte mit fester Breite ausgerichtet. Das heißt, die Bezeichnung wird sofort rechts neben dem Symbol angezeigt, anstatt zentriert zu sein. Dieser Stil kann nur mit dem TCS \_ FIXEDWIDTH-Stil verwendet werden und impliziert den TCS \_ FORCEICONLEFT-Stil.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**TCS \_ HOTTRACK**</dt> </dl>                            | [Version 4.70.](common-control-versions.md) Elemente unter dem Zeiger werden automatisch hervorgehoben. Sie können überprüfen, ob die Heiße Nachverfolgung aktiviert ist, indem [**Sie SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)aufrufen. <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**TCS \_ MULTILINE**</dt> </dl>                         | Bei Bedarf werden mehrere Zeilen mit Registerkarten angezeigt, sodass alle Registerkarten gleichzeitig sichtbar sind.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS \_ MULTISELECT**</dt> </dl>                   | [Version 4.70.](common-control-versions.md) Mehrere Registerkarten können ausgewählt werden, indem Sie beim Klicken die STRG-TASTE gedrückt halten. Dieser Stil muss mit dem TCS \_ BUTTONS-Stil verwendet werden.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**TCS \_ OWNERDRAWFIXED**</dt> </dl>          | Das übergeordnete Fenster ist für das Zeichnen von Registerkarten zuständig.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**TCS \_ RAGGEDRIGHT**</dt> </dl>                   | Zeilen mit Registerkarten werden nicht gestreckt, um die gesamte Breite des Steuerelements auszufüllen. Dieser Stil ist die Standardeinstellung.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS \_ RIGHT**</dt> </dl>                                     | [Version 4.70.](common-control-versions.md) Registerkarten werden vertikal auf der rechten Seite von Steuerelementen angezeigt, die den TCS \_ VERTICAL-Stil verwenden. Dieser Wert entspricht TCS \_ BOTTOM. Dieser Stil wird nicht unterstützt, wenn Sie visuelle Stile verwenden.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**TCS \_ RIGHTJUSTIFY**</dt> </dl>                | Die Breite jeder Registerkarte wird bei Bedarf erhöht, sodass jede Zeile mit Registerkarten die gesamte Breite des Registerkartensteuerelements ausfüllt. Dieser Fensterstil wird ignoriert, es sei denn, der TCS \_ MULTILINE-Stil wird ebenfalls angegeben.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**TCS \_ SCROLLOPPOSITE**</dt> </dl>          | [Version 4.70.](common-control-versions.md) Nicht benötigte Registerkarten scrollen zur gegenüberliegenden Seite des Steuerelements, wenn eine Registerkarte ausgewählt wird.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**TCS \_ SINGLELINE**</dt> </dl>                      | Es wird nur eine Zeile mit Registerkarten angezeigt. Der Benutzer kann bei Bedarf scrollen, um weitere Registerkarten anzuzeigen. Dieser Stil ist die Standardeinstellung.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**\_TCS-REGISTERKARTEN**</dt> </dl>                                        | Registerkarten werden als Registerkarten angezeigt, und ein Rahmen wird um den Anzeigebereich gezeichnet. Dieser Stil ist die Standardeinstellung.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**\_TCS-QUICKINFOS**</dt> </dl>                            | Dem Registerkartensteuerelement ist ein QuickInfo-Steuerelement zugeordnet. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ VERTICAL**</dt> </dl>                            | [Version 4.70.](common-control-versions.md) Registerkarten werden auf der linken Seite des Steuerelements angezeigt, wobei der Tabstopptext vertikal angezeigt wird. Dieser Stil ist nur gültig, wenn er mit dem TCS \_ MULTILINE-Stil verwendet wird. Damit Registerkarten auf der rechten Seite des Steuerelements angezeigt werden, verwenden Sie auch das TCS \_ RIGHT-Format. Dieser Stil wird nicht unterstützt, wenn Sie ComCtl32.dll Version 6 verwenden.<br/> |



## <a name="remarks"></a>Hinweise

Die folgenden Stile können geändert werden, nachdem das Steuerelement erstellt wurde.

-   TCS \_ BOTTOM
-   \_TCS-SCHALTFLÄCHEN
-   TCS \_ FIXEDWIDTH
-   TCS \_ FLATBUTTONS
-   TCS \_ FORCEICONLEFT
-   TCS \_ FORCELABELLEFT
-   TCS \_ MULTILINE
-   TCS \_ OWNERDRAWFIXED
-   TCS \_ RAGGEDRIGHT
-   TCS \_ RIGHT
-   TCS \_ VERTICAL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

