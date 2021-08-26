---
title: NM_CUSTOMDRAW(Trackbar)-Benachrichtigungscode (Commctrl.h)
description: Wird von einem Trackbar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW(Trackbar)-Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 6d863b180948676342a49615a526c8f6860905744aaf5269468807ad6dc04fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109550"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>NM \_ CUSTOMDRAW-Benachrichtigungscode (Trackleiste)

Wird von einem Trackbar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMCUSTOMDRAW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) die Informationen zum Zeichnungsvorgang enthält. Der **dwItemSpec-Member** dieser Struktur enthält einen der [benutzerdefinierten Zeichenwerte,](custom-draw-values.md) der angibt, welcher Teil des Steuerelements gezeichnet wird. Trackbar-Steuerelemente fügen die folgenden Werte in den **dwItemSpec-Member** dieser Struktur ein, um den Teil des steuerelements zu identifizieren, das gezeichnet wird:



| Wert                                                                                                                                                      | Bedeutung                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_TBCD-KANAL**</dt> </dl> | Identifiziert den Kanal, auf dem der Schieberegler des Trackbar-Steuerelements schiebet. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifiziert den Fingerabdruckmarker des Trackbar-Steuerelements. Dies ist der Teil des Steuerelements, den der Benutzer verschiebt. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**\_TBCD-TICS**</dt> </dl>          | Identifiziert die inkrementellen Teilstriche, die am Rand des Trackbar-Steuerelements angezeigt werden. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den Ihre Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwDrawStage-Member** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Das Steuerelement zeichnet sich selbst. Es werden keine [zusätzlichen NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) für diesen Farbzyklus gesendet. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Das Steuerelement benachrichtigt das übergeordnete Element über alle elementbezogenen Zeichnungsvorgänge. Sie sendet [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) vor und nach dem Zeichnen von Elementen. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Das Steuerelement benachrichtigt das übergeordnete Element nach dem Zeichnen eines Elements. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4.71.](common-control-versions.md) Das Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listenansichtsunterelement gezeichnet wird. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ PREPAINT ist.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. Das Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](custom-draw.md) Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Ihre Anwendung erstellt das Element manuell. Das Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.<br/>                                                                                                                                       |



 

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

 

 





