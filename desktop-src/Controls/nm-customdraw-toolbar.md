---
title: NM_CUSTOMDRAW (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einer Symbolleiste gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- NM_CUSTOMDRAW (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519319"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>NM- \_ Benachrichtigungs Code (Symbolleiste)

Wird von einer Symbolleiste gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4,70](common-control-versions.md). Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält. Der **dwitemspec** -Member dieser Struktur enthält den Befehls Bezeichner des Elements, das gezeichnet wird. Der **litemlparam** -Member dieser Struktur enthält den **dwdata** -Wert für das Element, das gezeichnet wird.

[Version 4,71](common-control-versions.md). Ein Zeiger auf eine [**nmtbcustomdraw**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält. Der **dwitemspec** -Member des **nmcd** -Members dieser Struktur enthält den Befehls Bezeichner des Elements, das gezeichnet wird. Der **litemlparam** -Member des **nmcd** -Members dieser Struktur enthält den **dwdata** -Wert für das Element, das gezeichnet wird.

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
| <dl> <dt>**tbcdrf- \_ blendion**</dt> </dl>       | [Version 5,00](common-control-versions.md). Mischen Sie die Schaltfläche 50 Prozent mit dem Hintergrund. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                      |
| <dl> <dt>**tbcdrf- \_ nobackground**</dt> </dl>    | [Version 5,00](common-control-versions.md). Der Schaltflächen Hintergrund wird nicht gezeichnet. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                        |
| <dl> <dt>**tbcdrf- \_ Knoten**</dt> </dl>         | [Version 4,71](common-control-versions.md). Keine Schaltflächen Ränder zeichnen. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                             |
| <dl> <dt>**tbcdrf \_ hilitehottrack**</dt> </dl>  | [Version 4,71](common-control-versions.md). Verwenden Sie den **clrhighlighthottrack** -Member der [**nmtbcustomdraw**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) -Struktur, um den Hintergrund von Elementen mit Hot-Nachverfolgung zu zeichnen. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                        |
| <dl> <dt>**tbcdrf- \_ nooffset**</dt> </dl>        | [Version 4,71](common-control-versions.md). Drücken Sie die Schaltfläche nicht, wenn Sie gedrückt werden. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                |
| <dl> <dt>**tbcdrf \_ nomark**</dt> </dl>          | Zeichnen Sie keine Standard Hervorhebung von Elementen, für die [**TBSTATE als \_ gekennzeichnet**](toolbar-button-states.md)ist. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                              |
| <dl> <dt>**tbcdrf \_ noetchedeffect**</dt> </dl>  | [Version 4,71](common-control-versions.md). Für deaktivierte Elemente werden keine geätzten Effekte gezeichnet. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                         |
| <dl> <dt>**tbcdrf \_ usecdcolors**</dt> </dl>     | [Version 6,00](common-control-versions.md), nur **Windows Vista** . Verwenden Sie benutzerdefinierte Zeichnungs Farben zum Rendering von Text, unabhängig vom visuellen Stil.<br/>                                                                                                                                         |



 

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

 

 





