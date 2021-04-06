---
description: Legt den Text eines Fensters fest.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: WM_SETTEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759493"
---
# <a name="wm_settext-message"></a>WM- \_ SetText-Nachricht

Legt den Text eines Fensters fest.


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Fenster Text ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist **true** , wenn der Text festgelegt ist. Es ist **false** (bei einem Bearbeitungs Steuerelement), **lb- \_ errspace** (für ein Listenfeld) oder **CB \_ errspace** (für ein Kombinations Feld), wenn nicht genügend Speicherplatz zum Festlegen des Texts im Bearbeitungs Steuerelement verfügbar ist. Es ist **CB \_ Err** , wenn diese Nachricht an ein Kombinations Feld ohne Bearbeitungs Steuerelement gesendet wird.

## <a name="remarks"></a>Bemerkungen

Mit der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion wird der Fenster Text festgelegt und angezeigt. Bei einem Bearbeitungs Steuerelement ist der Text der Inhalt des Bearbeitungs Steuer Elements. Bei einem Kombinations Feld ist der Text der Inhalt des Bearbeitungs Steuer Elements im Kombinations Feld. Für eine Schaltfläche ist der Text der Schaltflächen Name. Bei anderen Fenstern ist der Text der Fenstertitel.

Mit dieser Meldung wird die aktuelle Auswahl im Listenfeld eines Kombinations Felds nicht geändert. Eine Anwendung sollte die [**CB- \_ SelectString**](../controls/cb-selectstring.md) -Nachricht verwenden, um das Element in einem Listenfeld auszuwählen, das mit dem Text im Bearbeitungs Steuerelement übereinstimmt.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ gettext**](wm-gettext.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**CB- \_ SelectString**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
