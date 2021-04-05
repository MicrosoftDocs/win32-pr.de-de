---
description: Übertragung an jedes Fenster nach einem Design Änderungs Ereignis. Beispiele für Design Änderungs Ereignisse sind die Aktivierung eines Designs, die Deaktivierung eines Designs oder ein Übergang von einem Design zu einem anderen.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: WM_THEMECHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751200"
---
# <a name="wm_themechanged-message"></a>WM- \_ Nachricht

Übertragung an jedes Fenster nach einem Design Änderungs Ereignis. Beispiele für Design Änderungs Ereignisse sind die Aktivierung eines Designs, die Deaktivierung eines Designs oder ein Übergang von einem Design zu einem anderen.


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

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

> [!Note]  
> Diese Meldung wird vom Betriebssystem gepostet. Anwendungen senden diese Nachricht in der Regel nicht.

 

Designs sind Spezifikationen für die Darstellung von Steuerelementen, sodass das visuelle Element eines Steuer Elements getrennt von seiner Funktionalität behandelt wird.

Um ein vorhandenes Design Handle freizugeben, müssen Sie [**closeermedata**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)abrufen. Verwenden Sie zum Abrufen eines neuen Design Handles [**openfomedata**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

Nach der **WM \_** -Übertragung sind alle vorhandenen Design Handles ungültig. Ein Design fähiges Fenster sollte seine bereits vorhandenen Design Handles freigeben und erneut öffnen, wenn es die **WM \_** -Nachricht empfängt. Wenn die [**openrowmedata**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) -Funktion **null** zurückgibt, sollte das Fenster ohne Design gezeichnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Closethmedata**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**Isdermeactive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
