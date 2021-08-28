---
title: MCIWNDM_NOTIFYPOS (Vfw.h)
description: Die MCIWNDM NOTIFYPOS-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, \_ dass sich die Fensterposition geändert hat.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS-Nachricht Windows Multimedia
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
ms.openlocfilehash: d55d3b14ffb6a42e0c41cb820e066eee5c419b069e0d92ad614ffb51d577b963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428999"
---
# <a name="mciwndm_notifypos-message"></a>MCIWNDM \_ NOTIFYPOS-Nachricht

Die **MCIWNDM \_ NOTIFYPOS-Meldung** benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fensterposition geändert hat.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle für das MCIWnd-Fenster.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*Pos*
</dt> <dd>

Beschreibt die neue Position.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können die Benachrichtigung über Änderungen an der Position eines MCIWnd-Fensters aktivieren, indem Sie den MCIWNDF \_ NOTIFYPOS-Fensterstil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





