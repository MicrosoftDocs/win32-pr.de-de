---
title: TF_LBI_STYLE_ Konstanten (ctfutb. h)
description: Die TF \_ LBI \_ Style \_ \-Konstanten werden im dwstyle-Member der TF- \_ langbariteminfo-Struktur verwendet, um den Stil eines sprach leisten Elements anzugeben.
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
ms.openlocfilehash: 3b43ef805161afce6cb73bfaa26060308bc0aa5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476569"
---
# <a name="tf_lbi_style_-constants"></a>TF- \_ LBI- \_ Stil \_ \* Konstanten

Die **tf \_ LBI \_ Style \_ \* *_-Konstanten werden im _* dwstyle** -Member der [tf- \_ langbariteminfo](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) -Struktur verwendet, um den Stil eines sprach leisten Elements anzugeben.

Wenn dieser Stil mit \_ \_ der BTN-Schaltfläche für den TF LBI-Stil kombiniert wird \_ \_ , wird neben dem Text ein Dropdown Pfeil für das Element angezeigt. Der Dropdown Pfeil fungiert als Menü Schaltfläche, und durch Klicken auf die Schaltfläche wird **itflangbaritembutton:: InitMenu** aufgerufen. Wenn Sie auf den Textteil der Schaltfläche klicken, wird **itflangbaritembutton:: OnClick** aufgerufen.



| Konstante/Wert                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ hiddenstatus Control**</dt> <dt>0x00000001</dt> </dl> | Das Element kann \_ \_ \_ in der [itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) -Methode mit dem ausgeblendeten TF LBI-Status ausgeblendet oder dynamisch angezeigt werden. Wenn dieser Wert nicht vorhanden ist, kann das Element auf diese Weise nicht ausgeblendet werden.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ shownintray**</dt> <dt>0x00000002</dt> </dl>                         | Das Element wird zusätzlich zur sprach Leiste in der Benachrichtigungssymbol Leiste angezeigt. Dieses Flag wird derzeit nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ hideonnootheritems**</dt> <dt>0x00000004</dt> </dl>    | Die sprach Leiste ist ausgeblendet, wenn alle Elemente in der sprach Leiste diesen Stil enthalten. Wenn ein Element in der sprach Leiste diesen Stil nicht enthält, wird die sprach Leiste angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ shownintrayonly**</dt> <dt>0x00000008</dt> </dl>             | Das Element wird nur in der Benachrichtigungssymbol Leiste und nicht in der sprach Leiste angezeigt. Dieses Flag wird derzeit nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ hiddenbydefault**</dt> <dt>0x00000010</dt> </dl>             | Das Element wird erst dann auf der Symbolleiste angezeigt, wenn es im Menü Optionen für die sprach Leiste ausgewählt ist. Dieses Flag wird ignoriert, wenn der TF \_ LBI \_ -Stil " \_ hiddenstatuscontrol" festgelegt ist oder der Benutzer den ausgeblendeten/angezeigten Zustand im Menü "Optionen" der sprach Leiste bereits geändert hat.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ textcolorcon**</dt> <dt>0x00000020</dt> </dl>                   | Jedes schwarze Pixel innerhalb des Symbols wird in die Textfarbe des ausgewählten Designs konvertiert. Das Symbol muss ein Mono-Zeichen sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**Tf \_ \_ \_ BTN- \_ Schaltfläche für den LBI-Stil**</dt> <dt>0x00010000 bis</dt> </dl>                           | Das Element ist eine pushschaltfläche. [Itflangbaritembutton:: OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) wird aufgerufen, wenn das Element gedrückt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ BTN- \_ Menü**</dt> <dt>0x00020000</dt> </dl>                                 | Das Element ist ein Menü. [Itflangbaritembutton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) wird aufgerufen, wenn das Element gedrückt wird.<br/> Wenn dieser Stil mit \_ \_ der BTN-Schaltfläche für den TF LBI-Stil kombiniert wird \_ \_ , wird neben dem Text ein Dropdown Pfeil für das Element angezeigt. Der Dropdown Pfeil fungiert als Menü Schaltfläche, und durch Klicken auf die Schaltfläche wird **itflangbaritembutton:: InitMenu** aufgerufen. Wenn Sie auf den Textteil der Schaltfläche klicken, wird **itflangbaritembutton:: OnClick** aufgerufen.<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**Tf \_ LBI- \_ Stil \_ BTN \_**</dt> -umschalten <dt>0x00040000</dt> </dl>                           | Das Element ist eine UMSCHALT Fläche und funktioniert ähnlich wie ein Kontrollkästchen. **Itflangbaritembutton:: OnClick** wird aufgerufen, wenn das Element gedrückt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TF \_ langbariteminfo](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITF langbaritem:: GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[Itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





