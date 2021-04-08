---
title: MCIWNDM_NOTIFYMEDIA Meldung (VFW. h)
description: Die mciwndm \_ notifymedia-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass das Medium geändert wurde.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA-Nachricht (Multimedia)
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
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741152"
---
# <a name="mciwndm_notifymedia-message"></a>Mciwndm \_ notifymedia-Meldung

Die **mciwndm \_ notifymedia** -Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass das Medium geändert wurde.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das mciwnd-Fenster.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den neuen Dateinamen enthält. Wenn das Medium geschlossen wird, gibt es eine NULL-Zeichenfolge an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Benachrichtigung über Medien Änderungen aktivieren, indem Sie den Fenster Stil mciwndf \_ notifymedia angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





