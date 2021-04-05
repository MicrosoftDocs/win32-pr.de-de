---
description: Wird an ein Fenster gesendet, in dem der Benutzer die Größe ändert. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Größe und Position des Zieh Rechtecks überwachen und ggf. die Größe oder Position ändern.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: WM_SIZING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756631"
---
# <a name="wm_sizing-message"></a>Meldung zur WM- \_ Größe

Wird an ein Fenster gesendet, in dem der Benutzer die Größe ändert. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Größe und Position des Zieh Rechtecks überwachen und ggf. die Größe oder Position ändern.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Rand des Fensters mit der Größenanpassung. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                         | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**Wmsz \_ Unten**</dt> <dt>6</dt> </dl>                | Unterer Rand<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**Wmsz \_ BottomLeft**</dt> <dt>7</dt> </dl>    | Unten links<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**Wmsz \_ BottomRight**</dt> <dt>8</dt> </dl> | Unten rechts<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**Wmsz \_ Links**</dt> <dt>1</dt> </dl>                      | Linker Rand<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**Wmsz \_ Rechts**</dt> <dt>2</dt> </dl>                   | Rechter Rand<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**Wmsz \_ Top**</dt> <dt>3</dt> </dl>                         | Oberer Rand<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**Wmsz \_ TopLeft**</dt> <dt>4</dt> </dl>             | Linke obere Ecke<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**Wmsz \_ TopRight**</dt> <dt>5</dt> </dl>          | Obere rechte Ecke<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit den Bildschirm Koordinaten des Zieh Rechtecks. Um die Größe oder Position des Zieh Rechtecks zu ändern, muss eine Anwendung die Elemente dieser Struktur ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.

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

[**WM- \_ Bewegung**](wm-moving.md)
</dt> <dt>

[**WM- \_ Größe**](wm-size.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
