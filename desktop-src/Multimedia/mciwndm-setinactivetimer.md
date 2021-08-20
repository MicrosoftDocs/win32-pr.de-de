---
title: MCIWNDM_SETINACTIVETIMER Nachricht (Vfw.h)
description: Die MCIWNDM \_ SETINACTIVETIMER-Meldung legt den Aktualisierungszeitraum fest, der von MCIWnd verwendet wird, um die Trackleiste im MCIWnd-Fenster zu aktualisieren, die in der Titelleiste des Fensters angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungsmeldungen an das übergeordnete Fenster zu senden, wenn das MCIWnd-Fenster inaktiv ist. Sie können diese Nachricht explizit oder mithilfe des MCIWndSetInactiveTimer-Makros senden.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4161d52335e050fb8e9bcb702986492b5cd230713fcd15810a71590a92b030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137647"
---
# <a name="mciwndm_setinactivetimer-message"></a>MCIWNDM \_ SETINACTIVETIMER-Meldung

Die **MCIWNDM \_ SETINACTIVETIMER-Meldung** legt den Aktualisierungszeitraum fest, der von MCIWnd verwendet wird, um die Trackleiste im MCIWnd-Fenster zu aktualisieren, die in der Titelleiste des Fensters angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungsmeldungen an das übergeordnete Fenster zu senden, wenn das MCIWnd-Fenster inaktiv ist. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndSetInactiveTimer-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) senden.


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Inaktiv*
</dt> <dd>

Aktualisierungszeitraum in Millisekunden. Der Standardwert ist 2000 Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





