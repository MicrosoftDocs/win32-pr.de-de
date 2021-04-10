---
title: WM_CAP_FILE_SET_INFOCHUNK Meldung (VFW. h)
description: Die WM \_ \_ -Cap \_ -Datei Satz \_ -Infoblock-Nachricht legt Informationsblöcke fest und löscht diese.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK-Nachricht (Multimedia)
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
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040134"
---
# <a name="wm_cap_file_set_infochunk-message"></a>WM- \_ Abdeckungs \_ Datei \_ Satz- \_ infochunk-Nachricht

Die **WM- \_ Cap- \_ Datei Satz- \_ \_ Infoblock** -Nachricht legt Informationsblöcke fest und löscht diese. Informationsblöcke können während der Erfassung in eine AVI-Datei eingefügt werden, um Text Zeichenfolgen oder benutzerdefinierte Daten einzubetten. Sie können diese Nachricht explizit oder mithilfe des [**capflesetinfochunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) -Makros senden.


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpinfochunk*
</dt> <dd>

Ein Zeiger auf eine [**capinfochunk**](/windows/win32/api/vfw/ns-vfw-capinfochunk) -Struktur, die den zu erstellenden oder zu löschenden Informationsblock definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

Einer AVI-Datei können mehrere registrierte Informations Segmente hinzugefügt werden. Nachdem ein Informationsblock festgelegt wurde, wird er weiterhin zu nachfolgenden Erfassungs Dateien hinzugefügt, bis entweder der Eintrag gelöscht oder alle Informationsblock Einträge gelöscht werden. Um einen einzelnen Eintrag zu löschen, geben Sie die Informationen im Member **fccinfoid** und **null** im **lpdata** -Member der [**capinfochunk**](/windows/win32/api/vfw/ns-vfw-capinfochunk) -Struktur an. Wenn Sie alle Einträge löschen möchten, geben Sie **null** in **fccinfoid** an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





