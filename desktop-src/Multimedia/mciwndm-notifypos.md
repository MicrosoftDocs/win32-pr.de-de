---
title: MCIWNDM_NOTIFYPOS Meldung (VFW. h)
description: Die mciwndm \_ notifypos-Nachricht benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fensterposition geändert hat.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956970"
---
# <a name="mciwndm_notifypos-message"></a>Mciwndm \_ notifypos-Nachricht

Die **mciwndm \_ notifypos** -Nachricht benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fensterposition geändert hat.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das mciwnd-Fenster.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*POS*
</dt> <dd>

Beschreibt die neue Position.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Benachrichtigung über Änderungen an der Position eines mciwnd-Fensters aktivieren, indem Sie den Fenster Stil mciwndf \_ notifypos angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





