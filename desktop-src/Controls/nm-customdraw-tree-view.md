---
title: NM_CUSTOMDRAW -Benachrichtigungscode (Strukturansicht) (Commctrl.h)
description: Wird von einem Strukturansichtssteuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW -Benachrichtigungscode (Strukturansicht) Windows-Steuerelemente
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
ms.openlocfilehash: 9571d8461b43cebe047d80933af53a0c1aa1b865ede6280b8de2a33b74a60f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088840"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>NM \_ CUSTOMDRAW -Benachrichtigungscode (Strukturansicht)

Wird von einem Strukturansichtssteuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVCUSTOMDRAW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) die Informationen zum Zeichnungsvorgang enthält und empfängt. Der **dwItemSpec-Member** des **nmcd-Elements** dieser -Struktur enthält das Handle des elements, das gezeichnet wird. Das **lItemlParam-Element** des **nmcd-Elements** dieser -Struktur enthält die *lParam* des elements, das gezeichnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den Ihre Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwDrawStage-Member** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst. Es werden keine [zusätzlichen NM \_ CUSTOMDRAW-Codes](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Das -Steuerelement benachrichtigt das übergeordnete Element über elementbezogene Zeichnungsvorgänge. Sie sendet [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) vor und nach dem Zeichnen von Elementen. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Zeichnen eines Elements. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4.71.](common-control-versions.md) Das -Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listenansichtsunterelement gezeichnet wird. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. Das Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](custom-draw.md) Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Ihre Anwendung erstellt das Element manuell. Das Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

[Version 5.80.](common-control-versions.md) Wenn Sie die Schriftart ändern, indem Sie [**CDRF \_ NEWFONT**](cdrf-constants.md)zurückgeben, zeigt das Strukturansichtssteuerelement möglicherweise abgeschnittenen Text an. Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart eines Strukturansichtssteuerelements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) senden, bei der der *wParam-Wert* auf 5 festgelegt ist, bevor Sie dem Steuerelement Elemente hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von benutzerdefiniertem Zeichnen](custom-draw.md)
</dt> </dl>

 

 





