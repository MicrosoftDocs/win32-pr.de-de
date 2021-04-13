---
title: MCIWNDM_SETZOOM Meldung (VFW. h)
description: Die mciwndm- \_ Nachricht "setzoom" ändert die Größe eines Video Bilds entsprechend einem Zoomfaktor. Dadurch wird die Größe eines mciwnd-Fensters bei gleichzeitiger Beibehaltung eines konstanten Seitenverhältnisses angepasst. Sie können diese Nachricht explizit oder mithilfe des mciwndsetzoom-Makros senden.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475516"
---
# <a name="mciwndm_setzoom-message"></a>Mciwndm- \_ setzoom-Nachricht

Die **mciwndm-Nachricht " \_ setzoom** " ändert die Größe eines Video Bilds entsprechend einem Zoomfaktor. Dadurch wird die Größe eines mciwnd-Fensters bei gleichzeitiger Beibehaltung eines konstanten Seitenverhältnisses angepasst. Sie können diese Nachricht explizit oder mithilfe des [**mciwndsetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) -Makros senden.


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*izoom*
</dt> <dd>

Der Zoom Faktor, ausgedrückt als Prozentsatz des ursprünglichen Bilds. Geben Sie 100 an, um das Bild an der erstellten Größe anzuzeigen, 200, um das Bild bei der doppelten Größe anzuzeigen, oder 50, um das Bild in der Hälfte der normalen Größe anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndsetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





