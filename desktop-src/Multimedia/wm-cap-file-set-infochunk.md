---
title: WM_CAP_FILE_SET_INFOCHUNK-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ FILE SET \_ \_ INFOCHUNK-Meldung legt Informationsblöcke fest und löscht sie.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d64f88a87af63e5afc513e0e2cf2df53d64570bec099a2f8f2846d781fc0b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892070"
---
# <a name="wm_cap_file_set_infochunk-message"></a>WM \_ CAP FILE SET \_ \_ \_ INFOCHUNK-Meldung

Die **WM CAP FILE SET \_ \_ \_ \_ INFOCHUNK-Meldung** legt Informationsblöcke fest und löscht sie. Informationsblöcke können während der Erfassung in eine AVI-Datei eingefügt werden, um Textzeichenfolgen oder benutzerdefinierte Daten einzubetten. Sie können diese Nachricht explizit oder mithilfe des [**Makros capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) senden.


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Zeiger auf eine [**CAPINFOCHUNK-Struktur,**](/windows/win32/api/vfw/ns-vfw-capinfochunk) die den zu erstellenden oder zu löschenden Informationsabschnitt definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR-Meldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

## <a name="remarks"></a>Hinweise

Einer AVI-Datei können mehrere registrierte Informationsblöcke hinzugefügt werden. Nachdem ein Informationsblöcke festgelegt wurde, wird er den nachfolgenden Aufzeichnungsdateien hinzugefügt, bis entweder der Eintrag gelöscht oder alle Einträge für Informationsblöcke gelöscht wurden. Um einen einzelnen Eintrag zu löschen, geben Sie den Informationsabschnitt im **fccInfoID-Member** und **NULL** im **lpData-Member** der [**CAPINFOCHUNK-Struktur**](/windows/win32/api/vfw/ns-vfw-capinfochunk) an. Um alle Einträge zu löschen, geben Sie **NULL** in **fccInfoID an.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





