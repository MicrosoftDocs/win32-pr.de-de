---
description: Wird an ein Fenster gesendet, in dem die Größe des Benutzers geändert wird. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Größe und Position des Ziehrechtecks überwachen und bei Bedarf die Größe oder Position ändern.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: WM_SIZING Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645c9aaf778d5866050b45496298a46c4488e39b12f449f3ee0e8607dfc367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436155"
---
# <a name="wm_sizing-message"></a>\_WM-SIZING-Nachricht

Wird an ein Fenster gesendet, in dem die Größe des Benutzers geändert wird. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Größe und Position des Ziehrechtecks überwachen und bei Bedarf die Größe oder Position ändern.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Rand des Fensters, das dimensioniert wird. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                         | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_ BOTTOM**</dt> <dt>6</dt> </dl>                | Unterer Rand<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Untere linke Ecke<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Untere rechte Ecke<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ LEFT**</dt> <dt>1</dt> </dl>                      | Linker Rand<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ RIGHT**</dt> <dt>2</dt> </dl>                   | Rechter Rand<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_ TOP**</dt> <dt>3</dt> </dl>                         | Oberer Rand<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ TOPLEFT**</dt> <dt>4</dt> </dl>             | Linke obere Ecke<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_ TOPRIGHT**</dt> <dt>5</dt> </dl>          | Obere rechte Ecke<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) mit den Bildschirmkoordinaten des Ziehrechtecks. Um die Größe oder Position des Ziehrechtecks zu ändern, muss eine Anwendung die Elemente dieser Struktur ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte **TRUE** zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ MOVING**](wm-moving.md)
</dt> <dt>

[**\_WM-GRÖßE**](wm-size.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
