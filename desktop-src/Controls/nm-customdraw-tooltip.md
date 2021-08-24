---
title: NM_CUSTOMDRAW -Benachrichtigungscode (QuickInfo) (Commctrl.h)
description: Wird von einem QuickInfo-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW -Benachrichtigungscode (QuickInfo) Windows Controls
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
ms.openlocfilehash: cc75a12bdf216c03892656f25dd41ba93c35346cf5aead08758f917fec29bb8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816380"
---
# <a name="nm_customdraw-tooltip-notification-code"></a>NM \_ CUSTOMDRAW-Benachrichtigungscode (QuickInfo)

Wird von einem QuickInfo-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTTCUSTOMDRAW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) die Informationen zum Zeichnungsvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den Ihre Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Das **dwDrawStage-Element** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Das Steuerelement wird sich selbst zeichnen. Es werden keine zusätzlichen [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Das -Steuerelement benachrichtigt das übergeordnete Element über elementbezogene Zeichnungsvorgänge. Vor und nach dem Zeichnen von Elementen [werden NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                            |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Das -Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Das -Steuerelement benachrichtigt das übergeordnete Element, nachdem es ein Element gestrichen hat. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4.71](common-control-versions.md). Das -Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listenansichtsunteritem gezeichnet wird. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Die Anwendung hat eine neue Schriftart für das Element angegeben. Das -Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](custom-draw.md) Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Ihre Anwendung hat das Element manuell geerbt. Das -Steuerelement zeichnen das Element nicht. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                          |



 

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

 

 





