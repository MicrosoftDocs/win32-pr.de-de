---
title: MM_MOM_DONE (Mmsystem.h)
description: Die MM MOM DONE-Nachricht wird an ein Fenster gesendet, wenn der angegebene exklusive SYSTEM- oder Streampuffer wiedergegeben wurde und an \_ \_ die Anwendung zurückgegeben wird.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fcbcde545c7d29a313e729761c2e565db3405b10faf3156d9ef7dd0585b16b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807140"
---
# <a name="mm_mom_done-message"></a>MM \_ MOM \_ DONE-Nachricht

Die **MM \_ MOM \_ DONE-Nachricht** wird an ein Fenster gesendet, wenn der angegebene exklusive SYSTEM- oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle für das OUTPUT-Gerät des DEST-Geräts, das den Puffer wiedergegeben hat.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Zeiger auf eine [**DABEIHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) die den Puffer identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MESSAGES-Meldungen](midi-messages.md)
</dt> </dl>

 

