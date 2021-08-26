---
description: Legt den Text eines Fensters fest.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: WM_SETTEXT (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc2ab860fd89d726b9763c198fe8d58caa1376a3b919fd3587ad39a612d6667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055980"
---
# <a name="wm_settext-message"></a>WM \_ SETTEXT-Nachricht

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

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, bei der es sich um den Fenstertext handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist **TRUE,** wenn der Text festgelegt ist. Sie ist **FALSE** (für ein Bearbeitungssteuerfeld), **LB \_ ERRSPACE** (für ein Listenfeld) oder **CB \_ ERRSPACE** (für ein Kombinationsfeld), wenn nicht genügend Platz zum Festlegen des Texts im Bearbeitungssteuerfeld verfügbar ist. Es handelt **sich um CB \_ ERR,** wenn diese Nachricht ohne Bearbeitungssteuerfeld an ein Kombinationsfeld gesendet wird.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) legt den Fenstertext fest und zeigt den Text an. Bei einem Bearbeitungssteuerfeld ist der Text der Inhalt des Bearbeitungssteuerfelds. Für ein Kombinationsfeld ist der Text der Inhalt des Edit-Control-Teils des Kombinationsfelds. Bei einer Schaltfläche ist der Text der Schaltflächenname. Bei anderen Fenstern ist der Text der Fenstertitel.

Diese Meldung ändert nicht die aktuelle Auswahl im Listenfeld eines Kombinationsfelds. Eine Anwendung sollte die [**CB \_ SELECTSTRING-Meldung**](../controls/cb-selectstring.md) verwenden, um das Element in einem Listenfeld auszuwählen, das dem Text im Bearbeitungssteuerelement entspricht.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**CB \_ SELECTSTRING**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
