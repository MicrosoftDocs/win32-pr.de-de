---
title: Benachrichtigungs Code für NM_CUSTOMDRAW (QuickInfo) (kommstrg. h)
description: Wird von einem ToolTip-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW (QuickInfo)-Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743977"
---
# <a name="nm_customdraw-tooltip-notification-code"></a>NM \_ customdraw (QuickInfo)-Benachrichtigungs Code

Wird von einem ToolTip-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmttcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, der von der Anwendung zurückgegeben werden kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**cdrf \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst auf. Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                |
| <dl> <dt>**cdrf \_ notiteyitemdraw**</dt> </dl>    | Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                            |
| <dl> <dt>**cdrf \_ notifyposterase**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                 |
| <dl> <dt>**cdrf \_ notifypostpaint**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                |
| <dl> <dt>**cdrf \_ notifysubitemdraw**</dt> </dl> | [Version 4,71](common-control-versions.md). Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts-Unterelement gezeichnet wird. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                  |
| <dl> <dt>**cdrf \_ newFont**</dt> </dl>           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. Das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md). Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/> |
| <dl> <dt>**cdrf \_ skipdefault**</dt> </dl>       | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden benutzerdefinierter zeichnen](custom-draw.md)
</dt> </dl>

 

 





