---
title: MCIWNDM_NEW (Vfw.h)
description: Die Meldung MCIWNDM \_ NEW erstellt eine neue Datei für das aktuelle MCI-Gerät. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndNew senden.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bca9c03aff08c07f3ab1d8337547de776aeab5c6623a34ddaa71bfada0bca4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783080"
---
# <a name="mciwndm_new-message"></a>MCIWNDM \_ NEW-Nachricht

Die **Meldung MCIWNDM \_ NEW** erstellt eine neue Datei für das aktuelle MCI-Gerät. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) senden.


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf einen Puffer, der den Namen des MCI-Geräts enthält, das die Datei verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





