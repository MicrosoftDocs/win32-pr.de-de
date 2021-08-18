---
description: Stellt optionen dar, die beim Anzeigen eines Popupmenüs verfügbar sind.
title: MP_POPUPFLAGS konstanten (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1f6211769eca021f76fcbef34625f705cd3bf3fed02ca548d2965f17de80af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710010"
---
# <a name="mp_popupflags-constants"></a>MP \_ POPUPFLAGS-Konstanten

Stellt optionen dar, die beim Anzeigen eines Popupmenüs verfügbar sind.



| Konstante/Wert                                                                                                                                                                                                                               | Beschreibung                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_ SETFOCUS-0x00000001**</dt> <dt></dt> </dl>                | Geben Sie dem Popupmenü den Fokus.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_ INITIALSELECT-0x00000002**</dt> <dt></dt> </dl> | Wählen Sie das erste Element im Popupmenü aus.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_ NOANIMATE-0x00000004**</dt> <dt></dt> </dl>             | Verwenden Sie nicht die Standardsystemanimationen, z. B. einblenden, wenn Sie das Menü anzeigen.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_ TASTATUR**</dt> <dt>0X00000010</dt> </dl>                | Aktivieren Sie das Menü über eine Tastenkombination.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_ REPOSITION-0x00000020**</dt> <dt></dt> </dl>          | Zeigen Sie die Leiste basierend auf Änderungen am Menü an einer anderen Position an.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt> </dl>       | Reserviert. Darf nicht verwendet werden.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_ FINALSELECT-0x00000080**</dt> <dt></dt> </dl>       | Wählen Sie das letzte Element im Menü aus.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_ AUSRICHTUNG \_ NACH LINKS**</dt> <dt>0X02000000</dt> </dl>         | **Windows Vista oder** höher: Richten Sie das Popupmenü links neben dem Bereich aus, der im *prcExclude-Parameter* von [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**IMenuPopup::P opup angegeben**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)ist. Dies ist die Standardausrichtung.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_ AUSRICHTEN \_ NACH RECHTS**</dt> <dt>0x04000000</dt> </dl>      | **Windows Vista oder höher:** Richten Sie das Popupmenü rechts neben dem Bereich aus, der im *prcExclude-Parameter* von [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**IMenuPopup::P opup angegeben ist.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_ TOP**</dt> <dt>0x20000000</dt> </dl>                               | Positionieren Sie das Popupmenü über dem Anfangspunkt, der im *ppt-Parameter* von [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**IMenuPopup::P opup angegeben ist.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_ LEFT**</dt> <dt>0x40000000</dt> </dl>                            | Positionieren Sie das Popupmenü links vom Anfangspunkt.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_ RIGHT**</dt> <dt>0x60000000</dt> </dl>                         | Positionieren Sie das Popupmenü rechts vom Anfangspunkt.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_ BOTTOM**</dt> <dt>(int)0x80000000</dt> </dl>                 | Positionieren Sie das Popupmenü unterhalb des Anfangspunkts.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_ POS \_ MASK**</dt> <dt>(int)0xE0000000</dt> </dl>          | Die Menüpositionsmaske.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Hinweise

Diese Konstanten werden in der Datei Shobjidl.h definiert, beginnend mit Windows XP Service Pack 1 (SP1) und Windows Server 2003

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMenuPopup::P Opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu::P Opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




