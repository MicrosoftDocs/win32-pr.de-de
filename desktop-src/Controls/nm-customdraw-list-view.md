---
title: NM_CUSTOMDRAW (Listenansicht) Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansicht-Steuerelement gesendet, um seine übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW -Benachrichtigungscode (Listenansicht) Windows Controls
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
ms.openlocfilehash: d2b30af8dc61f9bb12d524f2b3f6ac58fb1adecebf66b4ad4477756e17f9a621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018872"
---
# <a name="nm_customdraw-list-view-notification-code"></a>NM \_ CUSTOMDRAW-Benachrichtigungscode (Listenansicht)

Wird von einem Listenansicht-Steuerelement gesendet, um seine übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVCUSTOMDRAW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) die Informationen zum Zeichnungsvorgang enthält. Der erste Member dieser -Struktur, **nmcd,** ist ein Zeiger auf eine [**NMCUSTOMDRAW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) Der **dwItemSpec-Member** der Struktur, auf die **nmcd** zeigt, enthält den Bezeichner des gezeichneten Elements, und das **lItemlParam-Element** enthält die anwendungsdefinierten Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den Ihre Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Das **dwDrawStage-Element** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Das Steuerelement wird sich selbst zeichnen. Es werden keine zusätzlichen [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | Windows Vista Das Steuerelement zeichnet nur den Hintergrund. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Das -Steuerelement benachrichtigt das übergeordnete Element über elementbezogene Zeichnungsvorgänge. Vor und nach dem Zeichnen von Elementen [werden NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) gesendet. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Das -Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Das -Steuerelement benachrichtigt das übergeordnete Element, nachdem es ein Element gestrichen hat. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Die Anwendung hat eine neue Schriftart für das Element angegeben. Das -Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](custom-draw.md) Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4.71.](common-control-versions.md) Ihre Anwendung erhält einen [NM \_ CUSTOMDRAW-Steuerungscode,](nm-customdraw.md) bei dem **dwDrawStage** auf CDDS \_ ITEMPREPAINT \| CDDS SUBITEM festgelegt ist, bevor jedes Unterelement der Listenansicht gezeichnet \_ wird. Anschließend können Sie Schriftart und Farbe für jedes Unterem separat angeben oder [**CDRF \_ DODEFAULT**](cdrf-constants.md) für die Standardverarbeitung zurückgeben. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Die Anwendung hat das Element manuell geerbt. Das -Steuerelement zeichnen das Element nicht. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Windows Vista Das Steuerelement zeichnen das Fokusrechteck nicht. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

[Version 5.80.](common-control-versions.md) Wenn Sie die Schriftart ändern, indem Sie [**CDRF \_ NEWFONT**](cdrf-constants.md)zurückgeben, zeigt das Listenansicht-Steuerelement möglicherweise abgeschnittenen Text an. Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart eines Listenansicht-Steuerelements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) mit dem *wParam-Wert* 5 senden, bevor Sie dem Steuerelement Elemente hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





