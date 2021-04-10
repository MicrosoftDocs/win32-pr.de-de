---
title: NM_CUSTOMDRAW (TrackBar)-Benachrichtigungs Code (kommctrl. h)
description: Wird von einem TrackBar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW (TrackBar)-Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106622"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>NM \_ (TrackBar)-Benachrichtigungs Code

Wird von einem TrackBar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält. Der **dwitemspec** -Member dieser Struktur enthält einen der [benutzerdefinierten zeichnen-Werte](custom-draw-values.md) , der angibt, welcher Teil des Steuer Elements gezeichnet wird. TrackBar-Steuerelemente fügen die folgenden Werte in den **dwitemspec** -Member dieser-Struktur ein, um den Teil des zu zeichnenden Steuer Elements zu identifizieren:



| Wert                                                                                                                                                      | Bedeutung                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**TBCD- \_ Kanal**</dt> </dl> | Gibt den Kanal an, entlang dem der Ziehpunkt des TrackBar-Steuer Elements bewegt wird. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD- \_ Thumb**</dt> </dl>       | Identifiziert den Zieh Punkt Marker des TrackBar-Steuer Elements. Dies ist der Teil des-Steuer Elements, den der Benutzer verschiebt. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD- \_ tik**</dt> </dl>          | Identifiziert die Inkrement-Teil Striche, die entlang der Kante des TrackBar-Steuer Elements angezeigt werden. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**cdrf \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst auf. Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                             |
| <dl> <dt>**cdrf \_ notiteyitemdraw**</dt> </dl>    | Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                         |
| <dl> <dt>**cdrf \_ notifyposterase**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                              |
| <dl> <dt>**cdrf \_ notifypostpaint**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                             |
| <dl> <dt>**cdrf \_ notifysubitemdraw**</dt> </dl> | [Version 4,71](common-control-versions.md). Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts-Unterelement gezeichnet wird. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                               |
| <dl> <dt>**cdrf \_ newFont**</dt> </dl>           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md). Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/> |
| <dl> <dt>**cdrf \_ skipdefault**</dt> </dl>       | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                       |



 

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

 

 





