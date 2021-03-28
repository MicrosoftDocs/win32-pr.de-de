---
description: Stellt Optionen dar, die beim Anzeigen eines Popup Menüs verfügbar sind.
title: MP_POPUPFLAGS Konstanten (shobjidl. h)
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
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130084"
---
# <a name="mp_popupflags-constants"></a>MP- \_ popupflags-Konstanten

Stellt Optionen dar, die beim Anzeigen eines Popup Menüs verfügbar sind.



| Konstante/Wert                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**Mppf \_ SetFocus**</dt> <dt>0x00000001</dt> </dl>                | Legen Sie dem Popupmenü den Fokus.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**Mppf \_ Initialselect**</dt> <dt>0x00000002</dt> </dl> | Wählen Sie das erste Element im Popup Menü aus.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**Mppf \_ Noanimieren**</dt> <dt>0x00000004</dt> </dl>             | Verwenden Sie beim Anzeigen des Menüs nicht die Standard systemanimationen, z. b. "ausblenden".<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**Mppf \_ Tastatur**</dt> <dt>0x00000010</dt> </dl>                | Aktivieren Sie das Menü mit einer Tastenkombination.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**Mppf \_ Neupositionieren**</dt> von <dt>0x00000020</dt> </dl>          | Zeigt die Leiste auf der Grundlage von Änderungen am Menü an einer anderen Position an.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**Mppf \_ Forcezorder**</dt> <dt>0x00000040</dt> </dl>       | Reserviert. Darf nicht verwendet werden.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**Mppf \_ Finalselect**</dt> <dt>0x00000080</dt> </dl>       | Wählen Sie das letzte Element im Menü aus.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**Mppf \_ \_Left**</dt> <dt>0x02000000</dt> ausrichten </dl>         | **Windows Vista oder** höher: richten Sie das Popup Menü links neben dem Bereich ein, der im *prcexclude* -Parameter von [**itrackshellmenu angegeben ist::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**imenupopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup). Dies ist die Standardausrichtung.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**Mppf \_ \_Rechts**</dt> bündig ausrichten <dt>0x04000000</dt> </dl>      | **Windows Vista oder** höher: richten Sie das Popup Menü rechts neben dem im *prcexclude* -Parameter von [**itrackshellmenu angegebenen Bereich ein::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**imenupopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**Mppf \_ Top**</dt> <dt>0x20000000</dt> </dl>                               | Positionieren Sie das Popup Menü oberhalb des Anfangs Punkts, der im *PPT* -Parameter von [**itrackshellmenu angegeben ist::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**imenupopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**Mppf \_ Left**</dt> <dt>0x40000000</dt> </dl>                            | Positionieren Sie das Popup Menü auf der linken Seite des Anfangs Punkts.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**Mppf \_ Right**</dt> <dt>0x60000000</dt> </dl>                         | Positionieren Sie das Popup Menü rechts neben dem Anfangspunkt.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**Mppf \_ Bottom**</dt> <dt>(int) 0x80000000</dt> </dl>                 | Positionieren Sie das Popup Menü unterhalb des Anfangs Punkts.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**Mppf \_ POS \_ Mask**</dt> <dt>(int) 0xE0000000</dt> </dl>          | Die Menü Positions Maske.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Bemerkungen

Diese Konstanten werden in der Datei "shobjidl. h" ab Windows XP Service Pack 1 (SP1) und Windows Server 2003 definiert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Imeinupopup::P-opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**Itrackshellmenu::P-opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




