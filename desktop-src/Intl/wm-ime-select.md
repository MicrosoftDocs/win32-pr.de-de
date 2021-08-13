---
description: Wird an eine Anwendung gesendet, wenn das Betriebssystem den aktuellen IME ändern wird. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: WM_IME_SELECT (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611ff30bac32fbd38c9aef00e459b49f9760d9702c619f7e6e7f55e6e3b10acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644620"
---
# <a name="wm_ime_select-message"></a>WM \_ IME \_ SELECT-Meldung

Wird an eine Anwendung gesendet, wenn das Betriebssystem den aktuellen IME ändern wird. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für ein Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Auswahlindikator. Dieser Parameter gibt **TRUE an,** wenn der angegebene IME ausgewählt ist. Der Parameter wird auf **FALSE festgelegt,** wenn der angegebene IME nicht mehr ausgewählt ist.

</dd> <dt>

*lParam* 
</dt> <dd>

Eingabe-Locale Identifier, der dem IME zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung, die ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben, damit sie das Tastaturlayouthand handle an den neu ausgewählten IME abrufen kann.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  verarbeitet diese Meldung, indem sie die Informationen an das STANDARD-IME-Fenster übergabe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Meldungen des Eingabemethode-Managers](input-method-manager-messages.md)
</dt> </dl>

 

 
