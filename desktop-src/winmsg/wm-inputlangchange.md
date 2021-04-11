---
description: Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabe Sprache einer Anwendung geändert wurde. Legen Sie alle anwendungsspezifischen Einstellungen fest, und übergeben Sie die Nachricht an die defwindowproc-Funktion, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128961"
---
# <a name="wm_inputlangchange-message"></a>WM- \_ inputlangchange-Meldung

Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabe Sprache einer Anwendung geändert wurde. Legen Sie alle anwendungsspezifischen Einstellungen fest, und übergeben Sie die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt. Diese untergeordneten Fenster können die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, damit Sie die Nachricht an ihre untergeordneten Fenster weiterleiten kann usw.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichensatz des neuen Gebiets Schemas.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Eingabe Gebiets Schema Bezeichner. Weitere Informationen finden Sie unter [Sprachen, Gebiets Schemas und Tastatur Layouts](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte bei der Verarbeitung dieser Nachricht einen Wert ungleich 0 (null) zurückgeben.

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

[**WM \_ inputlangchangerequest**](wm-inputlangchangerequest.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
