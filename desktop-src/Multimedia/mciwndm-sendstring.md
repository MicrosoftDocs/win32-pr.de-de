---
title: MCIWNDM_SENDSTRING Meldung (Vfw.h)
description: Die MCIWNDM \_ SENDSTRING-Nachricht sendet einen MCI-Befehl in Zeichenfolgenform an das Gerät, das dem MCIWnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des MCIWndSendString-Makros senden.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98ee008346821c2d489b19d01bb372c37cd3d541380fd8dae3b72bf613051f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037930"
---
# <a name="mciwndm_sendstring-message"></a>MCIWNDM \_ SENDSTRING-Nachricht

Die **MCIWNDM \_ SENDSTRING-Nachricht** sendet einen MCI-Befehl in Zeichenfolgenform an das Gerät, das dem MCIWnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndSendString-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) senden.


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*Sz*
</dt> <dd>

Zeichenfolgenbefehl, der an das MCI-Gerät gesendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der Nachrichtenhandler für **MCIWNDM \_ SENDSTRING** fügt einen Gerätealias an den MCI-Befehl an, den Sie an das Gerät senden. Daher sollten Sie keinen Alias in einem MCI-Befehl verwenden, den Sie mit **MCIWNDM \_ SENDSTRING** ausstellen.

Um die Rückgabezeichenfolge abzurufen, die das Ergebnis des Befehls enthält, senden Sie die [**MCIWNDM \_ RETURNSTRING-Nachricht.**](mciwndm-returnstring.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Multimediabefehlszeichenfolgen](multimedia-command-strings.md)
</dt> </dl>

 

 





