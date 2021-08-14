---
description: Wird nach einem Designänderungsereignis an jedes Fenster gesendet. Beispiele für Designänderungsereignisse sind die Aktivierung eines Designs, die Deaktivierung eines Designs oder ein Übergang von einem Design zu einem anderen.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: WM_THEMECHANGED-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b070cb492fa5db94acb97cd07f3de87455189d542aaaad2a51a3e0ecc6b4268d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199909"
---
# <a name="wm_themechanged-message"></a>WM \_ THEMECHANGED-Nachricht

Wird nach einem Designänderungsereignis an jedes Fenster gesendet. Beispiele für Designänderungsereignisse sind die Aktivierung eines Designs, die Deaktivierung eines Designs oder ein Übergang von einem Design zu einem anderen.


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter ist reserviert.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter ist reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Diese Meldung wird vom Betriebssystem gesendet. Anwendungen senden diese Nachricht in der Regel nicht.

 

Designs sind Spezifikationen für die Darstellung von Steuerelementen, sodass das visuelle Element eines Steuerelements getrennt von seiner Funktionalität behandelt wird.

Um ein vorhandenes Designhandle freizugeben, rufen [**Sie CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)auf. Verwenden Sie [**OpenThemeData,**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)um ein neues Designhandle zu erhalten.

Nach der **WM \_ THEMECHANGED-Übertragung** sind alle vorhandenen Designhandles ungültig. Ein designfähiges Fenster sollte alle bereits vorhandenen Designhandles freigeben und erneut öffnen, wenn die **WM \_ THEMECHANGED-Nachricht** empfangen wird. Wenn die [**OpenThemeData-Funktion**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) **NULL** zurückgibt, sollte das Fenster unbeschriftet zeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**Openthemedata**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
