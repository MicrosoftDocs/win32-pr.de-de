---
title: RF-Konstanten (CommCtrl.h)
description: Diese Konstanten werden als Rückgabewerte von einem Steuerelement als Reaktion auf einen NM \_ CUSTOMDRAW-Benachrichtigungscode verwendet.
ms.assetid: 6b05e27e-5d18-46f2-b326-2a5148597852
topic_type:
- apiref
api_name:
- CDRF_DODEFAULT
- CDRF_NEWFONT
- CDRF_SKIPDEFAULT
- CDRF_DOERASE
- CDRF_NOTIFYPOSTPAINT
- CDRF_NOTIFYITEMDRAW
- CDRF_NOTIFYSUBITEMDRAW
- CDRF_NOTIFYPOSTERASE
- CDRF_SKIPPOSTPAINT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817bab7c2ec41134d71c92ada94c62475b01cc2db96a9f8c74ecb2c7b9274451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770380"
---
# <a name="rf-constants"></a>RF-Konstanten

Diese Konstanten werden als Rückgabewerte von einem Steuerelement als Reaktion auf einen [NM \_ CUSTOMDRAW-Benachrichtigungscode](nm-customdraw.md) verwendet.



| Konstante/Wert                                                                                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**CDRF \_ DODEFAULT**</dt> <dt>0x00000000</dt> </dl>                         | Das Steuerelement zeichnet sich selbst. Es werden keine [zusätzlichen NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ PREPAINT entspricht.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**CDRF \_ NEWFONT**</dt> <dt>0x00000002</dt> </dl>                               | Die Anwendung hat eine neue Schriftart für das Element angegeben. Das Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter Ändern von Schriftarten und Farben. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ ITEMPREPAINT entspricht.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**CDRF \_ SKIPDEFAULT-0x00000004**</dt> <dt></dt> </dl>                   | Die Anwendung erstellt das Element manuell. Das Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ ITEMPREPAINT entspricht.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**CDRF \_ DOERASE**</dt> <dt>0x00000008</dt> </dl>                               | **Windows Vista und höher.** Das Steuerelement zeichnet den Hintergrund.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**CDRF \_ NOTIFYPOSTPAINT-0x00000010**</dt> <dt></dt> </dl>       | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Zeichnen eines Elements. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ PREPAINT entspricht.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> <dt>0x00000020</dt> </dl>          | Das Steuerelement benachrichtigt das übergeordnete Element über alle elementbezogenen Zeichnungsvorgänge. Sie sendet [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) vor und nach dem Zeichnen von Elementen. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ PREPAINT entspricht.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> <dt>0x00000020</dt> </dl> | **Internet Explorer 4.0 und höher.** Das Steuerelement benachrichtigt das übergeordnete Element über alle elementbezogenen Zeichnungsvorgänge. Sie sendet [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) vor und nach dem Zeichnen von Elementen. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ PREPAINT entspricht. Dieses Flag ist mit **CDRF \_ NOTIFYITEMDRAW** identisch, und seine Verwendung ist kontextabhängig.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> <dt>0x00000040</dt> </dl>       | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwDrawStage** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) CDDS \_ PREPAINT entspricht.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**CDRF \_ SKIPPOSTPAINT-0x00000100**</dt> <dt></dt> </dl>             | **Windows Vista und höher.** Das Steuerelement zeichnet das Fokusrechteck nicht.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Hinweise

Diese Konstanten werden in Commctrl.h definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen der Darstellung eines Steuerelements mit benutzerdefiniertem Zeichnen](custom-draw.md)
</dt> </dl>

 

 





