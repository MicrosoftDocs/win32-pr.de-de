---
title: WM_ASKCBFORMATNAME Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, um den Namen eines CF-Besitzer \_ Anzeige-Zwischenablage Formats anzufordern.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103251"
---
# <a name="wm_askcbformatname-message"></a>WM- \_ askcbformatname-Meldung

Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, um den Namen eines CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) -Zwischenablage Formats anzufordern.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Größe des Puffers in Zeichen, auf den der *LPARAM* -Parameter zeigt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der den Format Namen der Zwischenablage empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Als Antwort auf diese Nachricht sollte der Besitzer der Zwischenablage den Namen des Besitzers-Anzeige Formats in den angegebenen Puffer kopieren, wobei die vom *wParam* -Parameter angegebene Puffergröße nicht überschritten wird.

Ein Fenster der Zwischenablage Anzeige sendet diese Nachricht an den Besitzer der Zwischenablage, um den Namen des CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) Formats zu ermitteln, um z. b. eine Menü Liste mit verfügbaren Formaten zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Zwischenablage](clipboard.md)
</dt> </dl>

 

