---
title: TF_LBI_STYLE_ Konstanten (Ctfutb.h)
description: Die TF LBI STYLE \-Konstanten werden im dwStyle-Element der TF LANGBARITEMINFO-Struktur verwendet, um den Stil eines \_ \_ \_ \_ Sprachleistenelements anzugeben.
ms.assetid: 9180a666-774f-401b-bea3-68d5396fab30
topic_type:
- apiref
api_name:
- TF_LBI_STYLE_HIDDENSTATUSCONTROL
- TF_LBI_STYLE_SHOWNINTRAY
- TF_LBI_STYLE_HIDEONNOOTHERITEMS
- TF_LBI_STYLE_SHOWNINTRAYONLY
- TF_LBI_STYLE_HIDDENBYDEFAULT
- TF_LBI_STYLE_TEXTCOLORICON
- TF_LBI_STYLE_BTN_BUTTON
- TF_LBI_STYLE_BTN_MENU
- TF_LBI_STYLE_BTN_TOGGLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9954c416d9ad28f0ba0b2ddd6853b125039bf4db24adb3b3ff41f8722b2ba494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950795"
---
# <a name="tf_lbi_style_-constants"></a>TF \_ LBI \_ \_ \* STYLE-Konstanten

Die TF LBI STYLE _ -Konstanten werden **im \_ \_ \_ \* *_dwStyle-Element*** der TF [ \_ LANGBARITEMINFO-Struktur](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) verwendet, um den Stil eines Sprachleistenelements anzugeben.

Wenn dieser Stil mit TF LBI STYLE BTN BUTTON kombiniert wird, wird zusätzlich zum Text ein Dropdownpfeil für \_ \_ das Element \_ \_ angezeigt. Der Dropdownpfeil fungiert als Menüschaltfläche, und wenn Sie darauf klicken, wird **ITfLangBarItemButton::InitMenu** aufgerufen. Wenn Sie auf den Textteil der Schaltfläche klicken, wird **ITfLangBarItemButton::OnClick** aufgerufen.



| Konstante/Wert                                                                                                                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_ \_ \_ HIDDENSTATUSCONTROL-0X00000001**</dt> <dt></dt> </dl> | Das Element kann mithilfe des TF \_ LBI \_ STATUS \_ HIDDEN-Werts in der [ITfLangBarItem::GetStatus-Methode](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) ausgeblendet oder dynamisch angezeigt werden. Wenn dieser Wert nicht vorhanden ist, kann das Element nicht auf diese Weise ausgeblendet werden.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_ \_ \_ LBI-STIL, SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | Das Element wird zusätzlich zur Sprachleiste in der Benachrichtigungssymbolleiste angezeigt. Dieses Flag wird derzeit nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_ \_ \_ HIDEONNOOTHERITEMS**</dt> IM LBI-STIL <dt>0x00000004</dt> </dl>    | Die Sprachleiste wird ausgeblendet, wenn alle Elemente in der Sprachleiste diesen Stil enthalten. Wenn ein Element in der Sprachleiste diesen Stil nicht enthält, wird die Sprachleiste angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_ \_LBI-STIL \_ WIRD ANGEZEIGTINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | Das Element wird nur in der Taskleiste des Benachrichtigungssymbols und nicht in der Sprachleiste angezeigt. Dieses Flag wird derzeit nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_ \_LBI-STIL \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | Das Element wird erst auf der Symbolleiste angezeigt, wenn es im Menü mit den Sprachleistenoptionen ausgewählt wurde. Dieses Flag wird ignoriert, wenn TF LBI STYLE HIDDENSTATUSCONTROL festgelegt ist oder der Benutzer den ausgeblendeten/angezeigten Zustand bereits mithilfe des Menüs für Sprachleistenoptionen \_ \_ geändert \_ hat.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_ \_ \_ TEXTCOLORICON-0X00000020**</dt> <dt></dt> </dl>                   | Jedes schwarze Pixel innerhalb des Symbols wird in die Textfarbe des ausgewählten Designs konvertiert. Das Symbol muss monofarbig sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_ \_ \_ BTN-SCHALTFLÄCHE \_ IM LBI-STIL**</dt> <dt>0X00010000</dt> </dl>                           | Das Element ist eine Pushschaltfläche. [ITfLangBarItemButton::OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) wird aufgerufen, wenn das Element gedrückt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_ \_ \_ BTN-MENÜ IM \_ LBI-STIL**</dt> <dt>0X00020000</dt> </dl>                                 | Das Element ist ein Menü. [ITfLangBarItemButton::InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) wird aufgerufen, wenn das Element gedrückt wird.<br/> Wenn dieser Stil mit TF LBI STYLE BTN BUTTON kombiniert wird, wird zusätzlich zum Text ein Dropdownpfeil für \_ \_ das Element \_ \_ angezeigt. Der Dropdownpfeil fungiert als Menüschaltfläche, und wenn Sie darauf klicken, wird **ITfLangBarItemButton::InitMenu** aufgerufen. Wenn Sie auf den Textteil der Schaltfläche klicken, wird **ITfLangBarItemButton::OnClick** aufgerufen.<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_ \_ \_ BTN-UMSCHALTER IM \_ LBI-STIL**</dt> <dt>0x00040000</dt> </dl>                           | Das Element ist eine Umschaltfläche und funktioniert ähnlich wie ein Kontrollkästchen. **ITfLangBarItemButton::OnClick** wird aufgerufen, wenn das Element gedrückt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem::GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





