---
title: NM_CUSTOMDRAW Benachrichtigungscode (Rebar) (Commctrl.h)
description: Wird vom Rebar-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- NM_CUSTOMDRAW -Benachrichtigungscode (Rebar) Windows Controls
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
ms.openlocfilehash: 376bb9627d159dbb24080c2e475072dae357062975158d39f269e1cb7a4e3405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914870"
---
# <a name="nm_customdraw-rebar-notification-code"></a>NM \_ CUSTOMDRAW-Benachrichtigungscode (Rebar)

Wird vom Rebar-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMCUSTOMDRAW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) die Informationen zum Zeichnungsvorgang enthält. Der **dwItemSpec-Member** dieser -Struktur enthält den Bezeichner des gezeichneten Bands. Der **lItemlParam-Member** dieser -Struktur enthält den *lParam* des gezeichneten Bands.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den Ihre Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Das **dwDrawStage-Element** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Das Steuerelement wird sich selbst zeichnen. Es werden keine [zusätzlichen NM \_ CUSTOMDRAW-Benachrichtigungen](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Das -Steuerelement benachrichtigt das übergeordnete Element über elementbezogene Zeichnungsvorgänge. Vor und nach dem Zeichnen von Elementen [werden NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                           |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Das -Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Das -Steuerelement benachrichtigt das übergeordnete Element, nachdem es ein Element gestrichen hat. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                               |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | Das -Steuerelement benachrichtigt das übergeordnete Element über elementbezogene Zeichnungsvorgänge. Vor und nach dem Zeichnen von Elementen [werden NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                           |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Die Anwendung hat eine neue Schriftart für das Element angegeben. Das -Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](custom-draw.md) Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Die Anwendung hat das Element manuell geerbt. Das -Steuerelement zeichnen das Element nicht. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von benutzerdefiniertem Zeichnen](custom-draw.md)
</dt> </dl>

 

 





