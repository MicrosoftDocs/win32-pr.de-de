---
title: EM_INSERTIMAGE Meldung (RichEdit. h)
description: Ersetzt die Auswahl durch ein BLOB, das ein Bild anzeigt.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Windows-Steuerelemente für EM_INSERTIMAGE Meldung
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475558"
---
# <a name="em_insertimage-message"></a>EM \_ InsertImage-Nachricht

Ersetzt die Auswahl durch ein BLOB, das ein Bild anzeigt.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RichEdit- \_ Bild \_ Parameter**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) Struktur, die das bildblob enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                    | Beschreibung                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_** Fehler</dt> </dl>        | Das Bild kann nicht eingefügt werden. <br/>                          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>   | Der *LPARAM* -Parameter ist NULL oder zeigt auf ein ungültiges Bild. |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Wenn es sich bei der Auswahl um eine Einfügemarke handelt, wird das imageblob an der Einfügemarke eingefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ inserables**](em-inserttable.md)
</dt> </dl>

 

 





