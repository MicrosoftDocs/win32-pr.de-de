---
title: NM_CUSTOMDRAW (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
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
ms.openlocfilehash: 19d8927006f3a6a7e5543f2b072d24469a73a7ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106634"
---
# <a name="nm_customdraw-list-view-notification-code"></a>NM \_ customdraw (Listenansicht)-Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmlvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält. Der erste Member dieser Struktur, **nmcd**, ist ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur. Der **dwitemspec** -Member der Struktur, auf die von **nmcd** verwiesen wird, enthält den Bezeichner des Elements, das gezeichnet wird, und der **litemlparam** -Member enthält die Anwendungs definierten Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**cdrf \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst auf. Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**cdrf \_ doerase**</dt> </dl>           | Windows Vista Das-Steuerelement zeichnet das Fokus Rechteck nicht um ein Element. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**cdrf \_ notiteyitemdraw**</dt> </dl>    | Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**cdrf \_ notifyposterase**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**cdrf \_ notifypostpaint**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**cdrf \_ newFont**</dt> </dl>           | Die Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md). Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                                                              |
| <dl> <dt>**cdrf \_ notifysubitemdraw**</dt> </dl> | [Version 4,71.](common-control-versions.md) Die Anwendung empfängt einen [nm \_ customdraw](nm-customdraw.md) -Steuerungs Code, wobei **dwdrawstage** auf CDDs \_ itemprepaint \| CDDs \_ Unterelement festgelegt ist, bevor die einzelnen Listen Ansichts unter Elemente gezeichnet werden. Anschließend können Sie Schriftart und Farbe für jedes Unterelement separat angeben oder [**cdrf \_ DODEFAULT**](cdrf-constants.md) für die Standard Verarbeitung zurückgeben. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/> |
| <dl> <dt>**cdrf \_ skipdefault**</dt> </dl>       | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**cdrf \_ skippostpaint**</dt> </dl>     | Windows Vista Das-Steuerelement zeichnet nur den Hintergrund. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

[Version 5,80.](common-control-versions.md) Wenn Sie die Schriftart durch Zurückgeben von [**cdrf \_ newFont**](cdrf-constants.md)ändern, wird im Listenansicht-Steuerelement möglicherweise ein ausgeschnittener Text angezeigt. Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart eines Listenansicht-Steuer Elements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine ccm- [**\_ setVersion**](ccm-setversion.md) -Nachricht mit dem *wParam* -Wert 5 senden, bevor Sie dem Steuerelement Elemente hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





