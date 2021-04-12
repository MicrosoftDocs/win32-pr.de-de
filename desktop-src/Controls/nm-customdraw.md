---
title: NM_CUSTOMDRAW Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Zeichnungsvorgänge. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- Windows-Steuerelemente für NM_CUSTOMDRAW Benachrichtigungs
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475156"
---
# <a name="nm_customdraw-notification-code"></a>NM \_ customdraw-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Zeichnungsvorgänge. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine benutzerdefinierte Zeichnungs bezogene Struktur, die Informationen über den Zeichnungs Vorgang enthält. In der folgenden Liste sind die Steuerelemente und ihre zugeordneten Strukturen angegeben.



| Control                     | Benutzerdefinierte Zeichnungs Struktur                    |
|-----------------------------|------------------------------------------|
| Info Leiste, TrackBar und Header | [**Nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| Listenansicht                   | [**Nmlvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| QuickInfo                     | [**Nmttcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| Strukturansicht                   | [**Nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| Symbolleiste                     | [**Nmtbcustomdraw**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**cdrf \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst auf. Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet. Dieses Flag kann nicht mit einem anderen Flag verwendet werden. <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**cdrf \_ doerase**</dt> </dl>           | Das-Steuerelement zeichnet nur den Hintergrund.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**cdrf \_ newFont**</dt> </dl>           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md). Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                        |
| <dl> <dt>**cdrf \_ notiteyitemdraw**</dt> </dl>    | Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge. Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                |
| <dl> <dt>**cdrf \_ notifyposterase**</dt> </dl>   | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**cdrf \_ notifypostpaint**</dt> </dl>   | Das-Steuerelement sendet einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code, wenn der Zeichnungsprozess für das gesamte-Steuerelement vollständig ist. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**cdrf \_ notifysubitemdraw**</dt> </dl> | Die Anwendung empfängt einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code, wobei **dwdrawstage** auf CDDs \_ itemprepaint \| CDDs \_ Unterelement festgelegt ist, bevor die einzelnen Listen Ansichts unter Elemente gezeichnet werden. Anschließend können Sie Schriftart und Farbe für jedes Unterelement separat angeben oder [**cdrf \_ DODEFAULT**](cdrf-constants.md) für die Standard Verarbeitung zurückgeben. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/> |
| <dl> <dt>**cdrf \_ skipdefault**</dt> </dl>       | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**cdrf \_ skippostpaint**</dt> </dl>     | Das-Steuerelement zeichnet das Fokus Rechteck nicht um ein Element.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Derzeit unterstützen die folgenden Steuerelemente benutzerdefinierte Zeichnungsfunktionen: Header, Listenansicht, Info Leiste, Symbolleiste, QuickInfo, TrackBar und Strukturansicht. Benutzerdefiniertes Zeichnen wird auch für Schaltflächen Steuerelemente unterstützt, wenn Sie über ein Anwendungs Manifest verfügen, um sicherzustellen, dass Comctl32.dll Version 6 verfügbar ist

Wenn diese Meldung in einer Dialogfeld Prozedur behandelt wird, müssen Sie den Rückgabewert als Teil der Fenster Daten festlegen, bevor Sie " **true**" zurückgeben. Weitere Informationen finden Sie unter [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Licher**
</dt> <dt>

[Benutzerdefiniertes Zeichnen](custom-draw.md)
</dt> </dl>

 

