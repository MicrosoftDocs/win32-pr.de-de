---
title: WM_CLEAR Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM- \_ Clear-Meldung an ein Bearbeitungs Steuerelement oder Kombinations Feld, um die aktuelle Auswahl, sofern vorhanden, aus dem Bearbeitungs Steuerelement zu löschen (Löschen).
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR Nachrichten Datenaustausch
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
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339333"
---
# <a name="wm_clear-message"></a>WM- \_ Clear-Meldung

Eine Anwendung sendet eine **WM- \_ Clear** -Meldung an ein Bearbeitungs Steuerelement oder Kombinations Feld, um die aktuelle Auswahl, sofern vorhanden, aus dem Bearbeitungs Steuerelement zu löschen (Löschen).


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der von der WM- **\_ Clear** -Nachricht ausgeführte Löschvorgang kann rückgängig gemacht werden, indem das Bearbeitungs Steuerelement eine [**EM- \_ Rückgängig**](../controls/em-undo.md) -Meldung

Um die aktuelle Auswahl zu löschen und den gelöschten Inhalt in der Zwischenablage zu platzieren, verwenden Sie die [**WM- \_ Ausschneide**](wm-cut.md) Nachricht.

Beim Senden an ein Kombinations Feld wird die **WM \_** -Lösch Nachricht durch das Bearbeitungs Steuerelement behandelt. Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM- \_ Kopie**](wm-copy.md)
</dt> <dt>

[**WM \_ Ausschneiden**](wm-cut.md)
</dt> <dt>

[**WM \_ Einfügen**](wm-paste.md)
</dt> <dt>

[**WM \_ rückgängig machen**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

