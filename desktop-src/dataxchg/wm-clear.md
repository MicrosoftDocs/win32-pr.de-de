---
title: WM_CLEAR (Winuser.h)
description: Eine Anwendung sendet eine WM CLEAR-Nachricht an ein Bearbeitungssteuerfeld oder Kombinationsfeld, um die aktuelle Auswahl aus dem Bearbeitungssteuerfeld zu löschen \_ (löschen).
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR nachricht Data Exchange
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6820a9134f112b51474cd5b73e8545583cb02969b02a1bd1428138ebf1049dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029110"
---
# <a name="wm_clear-message"></a>WM \_ CLEAR-Meldung

Eine Anwendung sendet eine **WM \_ CLEAR-Nachricht** an ein Bearbeitungssteuerfeld oder Kombinationsfeld, um die aktuelle Auswahl aus dem Bearbeitungssteuerfeld zu löschen (löschen).


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der von der **WM \_ CLEAR-Nachricht durchgeführte** Löschvorgang kann rückgängig gemacht werden, indem dem Bearbeitungssteuerteil eine [**\_ EM-UNDO-Nachricht gesendet**](../controls/em-undo.md) wird.

Um die aktuelle Auswahl zu löschen und den gelöschten Inhalt in der Zwischenablage zu platzieren, verwenden Sie die [**WM \_ CUT-Meldung.**](wm-cut.md)

Wenn sie an ein Kombinationsfeld gesendet wird, wird die **WM \_ CLEAR-Nachricht** vom Bearbeitungssteuerfeld verarbeitet. Diese Meldung hat keine Auswirkungen, wenn sie an ein Kombinationsfeld mit dem [**CBS \_ DROPDOWNLIST-Format gesendet**](../controls/combo-box-styles.md) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ COPY**](wm-copy.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ PASTE**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

