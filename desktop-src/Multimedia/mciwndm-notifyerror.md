---
title: MCIWNDM_NOTIFYERROR Nachricht (Vfw.h)
description: Die MCIWNDM \_ NOTIFYERROR-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass ein MCI-Fehler aufgetreten ist.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dcca10f593c14e1532aa53b59b8c0bb106ea721ad0d09bde742727fddaeb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374131"
---
# <a name="mciwndm_notifyerror-message"></a>MCIWNDM \_ NOTIFYERROR-Meldung

Die **MCIWNDM \_ NOTIFYERROR-Meldung** benachrichtigt das übergeordnete Fenster einer Anwendung, dass ein MCI-Fehler aufgetreten ist.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle für das MCIWnd-Fenster.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*Errorcode*
</dt> <dd>

Numerischer Code für den MCI-Fehler.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können die MCI-Fehlerbenachrichtigung aktivieren, indem Sie das MCIWNDF \_ NOTIFYERROR-Fensterformat angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





