---
title: NM_CUSTOMDRAW (Listenansicht) Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansichtssteuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW -Benachrichtigungscode (Listenansicht) Windows-Steuerelemente
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
ms.openlocfilehash: ba991f5af43ee5513ec0713208aed84319bd5a9a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812672"
---
# <a name="nm_customdraw-list-view-notification-code"></a>NM \_ CUSTOMDRAW -Benachrichtigungscode (Listenansicht)

Wird von einem Listenansichtssteuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVCUSTOMDRAW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) die Informationen zum Zeichnungsvorgang enthält. Der erste Member dieser Struktur, **nmcd,** ist ein Zeiger auf eine [**NMCUSTOMDRAW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) Der **dwItemSpec-Member** der -Struktur, auf die **nmcd** zeigt, enthält den Bezeichner des elements, das gezeichnet wird, und der **lItemlParam-Member** enthält seine anwendungsdefinierten Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den Ihre Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwDrawStage-Member** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst. Es werden keine [zusätzlichen NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | Windows Vista Das Steuerelement zeichnet nur den Hintergrund. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Das Steuerelement benachrichtigt das übergeordnete Element über alle elementbezogenen Zeichnungsvorgänge. Sie sendet [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) vor und nach dem Zeichnen von Elementen. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Zeichnen eines Elements. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Die Anwendung hat eine neue Schriftart für das Element angegeben. Das Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](custom-draw.md) Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4.71.](common-control-versions.md) Ihre Anwendung empfängt einen [NM \_ CUSTOMDRAW-Steuerelementcode,](nm-customdraw.md) bei dem **dwDrawStage** auf CDDS \_ ITEMPREPAINT \| CDDS \_ SUBITEM festgelegt ist, bevor jedes Listenansichtsunterelement gezeichnet wird. Sie können dann schriftart und color für jedes Unteritem separat angeben oder [**CDRF \_ DODEFAULT**](cdrf-constants.md) für die Standardverarbeitung zurückgeben. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Die Anwendung erstellt das Element manuell. Das Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Windows Vista Das Steuerelement zeichnet das Fokusrechteck nicht. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

[Version 5.80.](common-control-versions.md) Wenn Sie die Schriftart ändern, indem Sie [**CDRF \_ NEWFONT**](cdrf-constants.md)zurückgeben, zeigt das Listenansichtssteuerelement möglicherweise abgeschnittenen Text an. Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart eines Listenansichtssteuerelements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) senden, bei der der *wParam-Wert* auf 5 festgelegt ist, bevor Sie dem Steuerelement Elemente hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





