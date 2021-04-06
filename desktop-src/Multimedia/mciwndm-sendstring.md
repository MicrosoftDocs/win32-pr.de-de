---
title: MCIWNDM_SENDSTRING Meldung (VFW. h)
description: Die mciwndm \_ sendstring-Nachricht sendet einen MCI-Befehl in Form einer Zeichenfolge an das Gerät, das dem mciwnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des mciwndsendstring-Makros senden.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING-Nachricht (Multimedia)
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
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742488"
---
# <a name="mciwndm_sendstring-message"></a>Mciwndm \_ sendstring-Nachricht

Die **mciwndm \_ sendstring** -Nachricht sendet einen MCI-Befehl in Form einer Zeichenfolge an das Gerät, das dem mciwnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) -Makros senden.


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*RT*
</dt> <dd>

Zeichen folgen Befehl, der an das MCI-Gerät gesendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Der Nachrichten Handler für **mciwndm \_ sendstring** fügt einen Gerätealias an den MCI-Befehl an, den Sie an das Gerät senden. Daher sollten Sie in einem MCI-Befehl, den Sie mit **mciwndm \_ sendstring** ausgeben, keinen Alias verwenden.

Um die Rückgabe Zeichenfolge, die das Ergebnis des Befehls enthält, zu erhalten, senden Sie die [**mciwndm-Nachricht " \_ returnstring**](mciwndm-returnstring.md) ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Multimediaregister](multimedia-command-strings.md)
</dt> </dl>

 

 





