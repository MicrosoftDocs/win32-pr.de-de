---
title: ICM_GETBUFFERSWANTED Meldung (VFW. h)
description: Die ICM \_ getbufferswanted-Nachricht fragt einen Treiber nach der Anzahl der zuzuordnenden Puffer ab. Sie können diese Nachricht explizit oder mit dem icgetbufferswanted-Makro senden.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949539"
---
# <a name="icm_getbufferswanted-message"></a>ICM \_ getbufferswanted-Nachricht

Die **ICM \_ getbufferswanted** -Nachricht fragt einen Treiber nach der Anzahl der zuzuordnenden Puffer ab. Sie können diese Nachricht explizit oder mit dem [**icgetbufferswanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) -Makro senden.


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwbuffers*
</dt> <dd>

Adresse, die die Anzahl der Abtastungen enthält, die der Treiber zum effizienten Rendering der Daten benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR OK zurück, \_ andernfalls wird ICERR \_ nicht unterstützt.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird von Treibern verwendet, die Hardware zum Rendering von Daten verwenden und eine minimale Zeitverzögerung sicherstellen möchten, die durch warten auf das Eintreffen von Puffern verursacht wird. Wenn ein Treiber z. b. ein Video Dekomprimierungs Board steuert, das 10 Videorahmen aufnehmen kann, kann es für diese Nachricht 10 zurückgeben. Dadurch werden Anwendungen angewiesen, 10 Frames vor dem Frame zu behalten, den Sie zurzeit benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





