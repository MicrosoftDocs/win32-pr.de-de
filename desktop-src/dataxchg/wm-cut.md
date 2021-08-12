---
title: WM_CUT Meldung (Winuser.h)
description: Eine Anwendung sendet eine WM \_ CUT-Nachricht an ein Bearbeitungssteuerelement oder Kombinationsfeld, um ggf. die aktuelle Auswahl im Bearbeitungssteuerelement zu löschen (ausschneiden) und den gelöschten Text im CF TEXT-Format in die Zwischenablage zu \_ kopieren.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT-Nachricht Data Exchange
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
ms.openlocfilehash: d117e0a942c0d9e24e1a9c40d3d66e605ab8d5cf26bbad0e287e9b03a9b25780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304493"
---
# <a name="wm_cut-message"></a>WM \_ CUT-Nachricht

Eine Anwendung sendet eine **WM \_ CUT-Nachricht** an ein Bearbeitungssteuerelement oder Kombinationsfeld, um ggf. die aktuelle Auswahl im Bearbeitungssteuerelement zu löschen (ausschneiden) und den gelöschten Text im [**CF \_ TEXT-Format**](standard-clipboard-formats.md) in die Zwischenablage zu kopieren.


```C++
#define WM_CUT                          0x0300
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

Der von der **WM \_ CUT-Nachricht** ausgeführte Löschvorgang kann rückgängig werden, indem dem Bearbeitungssteuerelement eine [**\_ EM-UNDO-Nachricht**](../controls/em-undo.md) gesendet wird.

Verwenden Sie die [**WM \_ CLEAR-Meldung,**](wm-clear.md) um die aktuelle Auswahl zu löschen, ohne den gelöschten Text in der Zwischenablage zu platzieren.

Wenn die **WM \_ CUT-Nachricht** an ein Kombinationsfeld gesendet wird, wird sie vom Bearbeitungssteuerelement verarbeitet. Diese Meldung hat keine Auswirkungen, wenn sie an ein Kombinationsfeld mit dem [**\_ CBS-DROPDOWNLIST-Format**](../controls/combo-box-styles.md) gesendet wird.

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

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ COPY**](wm-copy.md)
</dt> <dt>

[**\_WM-EINFÜGE**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**EM \_ UNDO**](../controls/em-undo.md)
</dt> </dl>

 

