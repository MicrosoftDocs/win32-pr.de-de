---
title: MCIWNDM_VALIDATEMEDIA Meldung (VFW. h)
description: Die mciwndm \_ validatemedia-Nachricht aktualisiert die Start-und Endpositionen des Inhalts, die aktuelle Position im Inhalt und die TrackBar gemäß dem aktuellen Zeitformat.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517411"
---
# <a name="mciwndm_validatemedia-message"></a>Mciwndm \_ validatemedia-Meldung

Die **mciwndm \_ validatemedia** -Nachricht aktualisiert die Start-und Endpositionen des Inhalts, die aktuelle Position im Inhalt und die TrackBar gemäß dem aktuellen Zeitformat. Sie können diese Nachricht explizit oder mithilfe des [**mciwndvalidatemedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) -Makros senden.


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In der Regel sollten Sie dieses Makro nicht verwenden. Wenn Ihre Anwendung jedoch das Zeitformat eines Geräts ohne Verwendung von mciwnd ändert, die Start-und Endpositionen des Inhalts sowie die TrackBar verwenden weiterhin das alte Format. Mit diesem Makro können Sie diese Werte aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndvalidatemedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





