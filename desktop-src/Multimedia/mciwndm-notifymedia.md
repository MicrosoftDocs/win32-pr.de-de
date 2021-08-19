---
title: MCIWNDM_NOTIFYMEDIA (Vfw.h)
description: Die MCIWNDM NOTIFYMEDIA-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, \_ dass sich das Medium geändert hat.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa64b17fb3910e518e5b5d4318f8d988cf71f8c314f047a5f2eed1ff80cc843d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783021"
---
# <a name="mciwndm_notifymedia-message"></a>MCIWNDM \_ NOTIFYMEDIA-Nachricht

Die **MCIWNDM \_ NOTIFYMEDIA-Meldung** benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich das Medium geändert hat.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle für das MCIWnd-Fenster.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den neuen Dateinamen enthält. Wenn das Medium geschlossen wird, gibt es eine NULL-Zeichenfolge an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können die Benachrichtigung über Medienänderungen aktivieren, indem Sie den MCIWNDF \_ NOTIFYMEDIA-Fensterstil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





