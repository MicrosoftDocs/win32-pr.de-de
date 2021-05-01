---
description: Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabesprache einer Anwendung geändert wurde. Sie sollten anwendungsspezifische Einstellungen vornehmen und die Nachricht an die DefWindowProc-Funktion übergeben, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332405"
---
# <a name="wm_inputlangchange-message"></a>WM \_ INPUTLANGCHANGE-Nachricht

Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabesprache einer Anwendung geändert wurde. Sie sollten anwendungsspezifische Einstellungen vornehmen und die Nachricht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt. Diese untergeordneten Fenster können die Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, damit die Nachricht an ihre untergeordneten Fenster übergeben wird usw.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam*

</dt> <dd>
  
Typ: **WPARAM**

Die [Codepage](../Intl/code-pages.md) des neuen Gebietsschemas.

</dd> <dt>

*lParam*

</dt> <dd>
 
Typ: **LPARAM**

Der  HKL-Eingabe-Gebietsschemabezeichner. Weitere Informationen finden Sie unter [Sprachen, Gebietsschemas und Tastaturlayouts.](../inputdev/about-keyboard-input.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte einen Wert ungleich 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Sie können den [Namen des Tastaturschemas](../Intl/locale-names.md) über [die LCIDToLocaleName-Funktion](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) abrufen. Mit dem Gebietsschemanamen können Sie [moderne Gebietsschemafunktionen](/windows/win32/intl/calling-the--locale-name--functions)verwenden:

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>Anforderungen

| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

**Verweis**

- [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**WM \_ INPUTLANGCHANGEREQUEST**](wm-inputlangchangerequest.md)

**Konzept**

- [Windows](windows.md) 
