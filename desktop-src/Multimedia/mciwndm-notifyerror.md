---
title: MCIWNDM_NOTIFYERROR Meldung (VFW. h)
description: Die mciwndm \_ notifyerror-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass ein MCI-Fehler aufgetreten ist.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR-Nachricht (Multimedia)
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
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040479"
---
# <a name="mciwndm_notifyerror-message"></a>Mciwndm \_ notifyerror-Meldung

Die **mciwndm \_ notifyerror** -Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass ein MCI-Fehler aufgetreten ist.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das mciwnd-Fenster.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*ErrorCode*
</dt> <dd>

Numerischer Code für den MCI-Fehler.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die MCI-Fehler Benachrichtigung aktivieren, indem Sie den Fenster Stil "mciwndf \_ notifyerror" angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





