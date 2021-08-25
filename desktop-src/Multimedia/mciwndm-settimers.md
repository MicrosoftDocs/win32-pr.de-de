---
title: MCIWNDM_SETTIMERS (Vfw.h)
description: Die MCIWNDM SETTIMERS-Meldung legt die Aktualisierungszeiträume fest, die von MCIWnd verwendet werden, um die Trackleiste im MCIWnd-Fenster zu aktualisieren, die in der Titelleiste des Fensters angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungsmeldungen an das übergeordnete Fenster zu \_ senden.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9c17a131827459555ae51adc5d5bd48d98fabb88fc4c1f0dbbcd1eb3673466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807555"
---
# <a name="mciwndm_settimers-message"></a>MCIWNDM \_ SETTIMERS-Meldung

Die **MCIWNDM \_ SETTIMERS-Meldung** legt die Aktualisierungszeiträume fest, die von MCIWnd verwendet werden, um die Trackleiste im MCIWnd-Fenster zu aktualisieren, die in der Titelleiste des Fensters angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungsmeldungen an das übergeordnete Fenster zu senden. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndSetTimers-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) senden.


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*aktiv*
</dt> <dd>

Aktualisierungszeitraum, der von MCIWnd verwendet wird, wenn es sich um das aktive Fenster handelt. Der Standardwert ist 500 Millisekunden. Storage für diesen Wert ist auf 16 Bits beschränkt.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Inaktiv*
</dt> <dd>

Aktualisierungszeitraum, der von MCIWnd verwendet wird, wenn es sich um das inaktive Fenster handelt. Der Standardwert beträgt 2.000 Millisekunden. Storage für diesen Wert ist auf 16 Bits beschränkt.

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

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





