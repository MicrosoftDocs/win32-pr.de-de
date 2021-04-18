---
title: WM_CUT Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM \_ -Ausschneide Nachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um die aktuelle Auswahl (sofern vorhanden) im Bearbeitungs Steuerelement zu löschen (Ausschneiden) und den gelöschten Text im CF-Textformat in die Zwischenablage zu kopieren \_ .
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338332"
---
# <a name="wm_cut-message"></a>WM- \_ Ausschneide Nachricht

Eine Anwendung sendet eine **WM- \_ Ausschneide** Nachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um die aktuelle Auswahl (sofern vorhanden) im Bearbeitungs Steuerelement zu löschen (Ausschneiden) und den gelöschten Text im [**CF- \_ Text**](standard-clipboard-formats.md) Format in die Zwischenablage zu kopieren.


```C++
#define WM_CUT                          0x0300
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

Der von der WM- **\_ Ausschneide** Nachricht ausgeführte Löschvorgang kann rückgängig gemacht werden, indem das Bearbeitungs Steuerelement eine [**EM- \_ Rückgängig**](../controls/em-undo.md) -Meldung

Um die aktuelle Auswahl zu löschen, ohne den gelöschten Text in der Zwischenablage zu platzieren, verwenden Sie die unverschlüsselte [**WM \_**](wm-clear.md) -Nachricht.

Beim Senden an ein Kombinations Feld wird die **WM- \_ Ausschneide** Nachricht durch das Bearbeitungs Steuerelement behandelt. Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.

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

[**WM \_ Clear**](wm-clear.md)
</dt> <dt>

[**WM- \_ Kopie**](wm-copy.md)
</dt> <dt>

[**WM \_ Einfügen**](wm-paste.md)
</dt> <dt>

[**WM \_ rückgängig machen**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**EM \_ rückgängig machen**](../controls/em-undo.md)
</dt> </dl>

 

