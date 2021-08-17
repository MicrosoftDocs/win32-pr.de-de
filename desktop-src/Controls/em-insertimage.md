---
title: EM_INSERTIMAGE Nachricht (Richedit.h)
description: Ersetzt die Auswahl durch ein Blob, das ein Bild anzeigt.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 7418a8fe4b7c627d211bce7bf2591ed684d82e42089fbe9bedeb2f76a6b9d3e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437890"
---
# <a name="em_insertimage-message"></a>EM \_ INSERTIMAGE-Nachricht

Ersetzt die Auswahl durch ein Blob, das ein Bild anzeigt.


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

Ein Zeiger auf eine [**RICHEDIT \_ IMAGE \_ PARAMETERS-Struktur,**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) die das Imageblob enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                    | Beschreibung                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Das Bild kann nicht eingefügt werden. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Der *lParam-Parameter* ist NULL oder verweist auf ein ungültiges Bild. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Wenn die Auswahl eine Einfügemarke ist, wird das Bildblob an der Einfügemarke eingefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ INSERTTABLE**](em-inserttable.md)
</dt> </dl>

 

 





