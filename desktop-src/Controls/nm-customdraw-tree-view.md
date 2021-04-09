---
title: Benachrichtigungs Code für NM_CUSTOMDRAW (Strukturansicht) (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858652"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>NM \_ customdraw (Strukturansicht)-Benachrichtigungs Code

Wird von einem Strukturansicht-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält und empfängt. Der **dwitemspec** -Member des **nmcd** -Members dieser Struktur enthält das Handle des Elements, das gezeichnet wird. Der **litemlparam** -Member des **nmcd** -Members dieser Struktur enthält den *LPARAM* -Element des Elements, das gezeichnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**cdrf \_ DODEFAULT**</dt> </dl>         | Das-Steuerelement zeichnet sich selbst. Es werden keine zusätzlichen nm- [ \_ customdraw](nm-customdraw.md) -Codes für diesen Zeichnungs Kreis gesendet. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                              |
| <dl> <dt>**cdrf \_ notiteyitemdraw**</dt> </dl>    | Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Es sendet [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes vor und nach dem Zeichnen von Elementen. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                |
| <dl> <dt>**cdrf \_ notifyposterase**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                  |
| <dl> <dt>**cdrf \_ notifypostpaint**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                |
| <dl> <dt>**cdrf \_ notifysubitemdraw**</dt> </dl> | [Version 4,71.](common-control-versions.md) Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts Unterelement gezeichnet wird. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                  |
| <dl> <dt>**cdrf \_ newFont**</dt> </dl>           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md). Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/> |
| <dl> <dt>**cdrf \_ skipdefault**</dt> </dl>       | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

[Version 5,80.](common-control-versions.md) Wenn Sie die Schriftart ändern, indem Sie [**cdrf \_ newFont**](cdrf-constants.md)zurückgeben, wird im Strukturansicht-Steuerelement möglicherweise der abgeschnittene Text angezeigt. Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart eines Strukturansicht-Steuer Elements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine ccm- [**\_ setVersion**](ccm-setversion.md) -Nachricht mit dem *wParam* -Wert 5 senden, bevor Sie dem Steuerelement Elemente hinzufügen.

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

 

 





