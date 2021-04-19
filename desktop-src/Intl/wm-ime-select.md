---
description: Wird an eine Anwendung gesendet, wenn das Betriebssystem im Begriff ist, den aktuellen IME zu ändern. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: WM_IME_SELECT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345732"
---
# <a name="wm_ime_select-message"></a>WM- \_ IME \_ Select-Nachricht

Wird an eine Anwendung gesendet, wenn das Betriebssystem im Begriff ist, den aktuellen IME zu ändern. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Auswahl Indikator. Dieser Parameter gibt **true** an, wenn der angegeben IME ausgewählt ist. Der-Parameter wird auf **false** festgelegt, wenn der angegebene IME nicht mehr ausgewählt ist.

</dd> <dt>

*lParam* 
</dt> <dd>

Eingabe Gebiets Schema Bezeichner, der dem IME zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung, die ein IME-Fenster erstellt hat, sollte diese Nachricht an dieses Fenster übergeben, damit Sie das Tastaturlayout-Handle für die neu ausgewählte IME abrufen kann.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion verarbeitet diese Nachricht, indem Sie die Informationen an das IME-Standardfenster übergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Meldungen](input-method-manager-messages.md)
</dt> </dl>

 

 
