---
title: RF-Konstanten (kommctrl. h)
description: Diese Konstanten werden als Rückgabewerte von einem-Steuerelement als Antwort auf einen nm \_ customdraw-Benachrichtigungs Code verwendet.
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
ms.openlocfilehash: 15ec83b8f8238e4236bbee3f7091c228c552efb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364687"
---
# <a name="rf-constants"></a>RF-Konstanten

Diese Konstanten werden als Rückgabewerte von einem-Steuerelement als Antwort auf einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code verwendet.



| Konstante/Wert                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**Cdrf \_ DODEFAULT**</dt> <dt>0x00000000</dt> </dl>                         | Das Steuerelement zeichnet sich selbst auf. Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur dem CDDs- \_ präpaint entspricht.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**Cdrf \_ Neuschriftart**</dt> <dt>0x00000002</dt> </dl>                               | Die Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter Ändern von Schriftarten und Farben. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur CDDs \_ itemprepaint entspricht.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**Cdrf \_ Skipdefault**</dt> <dt>0x00000004</dt> </dl>                   | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur CDDs \_ itemprepaint entspricht.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**Cdrf \_ Doerase**</dt> <dt>0x00000008</dt> </dl>                               | **Windows Vista und höher.** Das-Steuerelement zeichnet den Hintergrund.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**Cdrf \_ Notifypostpaint**</dt> <dt>0x00000010</dt> </dl>       | Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur dem CDDs- \_ präpaint entspricht.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**Cdrf \_ Notiteyitemdraw**</dt> <dt>0x00000020</dt> </dl>          | Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur dem CDDs- \_ präpaint entspricht.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**Cdrf \_ Notifysubitemdraw**</dt> <dt>0x00000020</dt> </dl> | **Internet Explorer 4,0 und höher.** Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur dem CDDs- \_ präpaint entspricht. Dieses Flag ist mit **cdrf \_ notifyitemdraw** identisch, und seine Verwendung ist Kontext abhängig.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**Cdrf \_ Notifyposterase**</dt> <dt>0x00000040</dt> </dl>       | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn die **dwdrawstage** der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur dem CDDs- \_ präpaint entspricht.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**Cdrf \_ Skippostpaint**</dt> <dt>0x00000100</dt> </dl>             | **Windows Vista und höher.** Das-Steuerelement zeichnet das Fokus Rechteck nicht.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Bemerkungen

Diese Konstanten werden in "kommctrl. h" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen des Erscheinungs Bilds eines Steuer Elements mithilfe von benutzerdefiniertem zeichnen](custom-draw.md)
</dt> </dl>

 

 





