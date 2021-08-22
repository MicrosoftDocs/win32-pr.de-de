---
title: ICM_GETBUFFERSWANTED (Vfw.h)
description: Die ICM GETBUFFERSWANTED fragt einen Treiber nach der Anzahl der zu \_ reservierenden Puffer ab. Sie können diese Nachricht explizit oder mithilfe des Makros ICGetBuffersWanted senden.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED-Nachricht Windows Multimedia
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
ms.openlocfilehash: c4bd5fae6e9f008649366cf922ef117f5b6f7560a7764c4f8d81552a255de48a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495870"
---
# <a name="icm_getbufferswanted-message"></a>\_ICM GETBUFFERSWANTED-Nachricht

Die **ICM \_ GETBUFFERSWANTED** fragt einen Treiber nach der Anzahl der zu reservierenden Puffer ab. Sie können diese Nachricht explizit oder mithilfe des [**Makros ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) senden.


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Adresse, die die Anzahl der Stichproben enthält, die der Treiber benötigt, um die Daten effizient zu rendern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, andernfalls ICERR \_ UNSUPPORTED.

## <a name="remarks"></a>Hinweise

Diese Meldung wird von Treibern verwendet, die Hardware zum Rendern von Daten verwenden und eine minimale Zeitverzögerung sicherstellen möchten, die durch das Warten auf das Eintreffen von Puffern verursacht wird. Wenn ein Treiber beispielsweise ein Videodekomprimierungsboard steuert, das 10 Videoframes enthält, kann er für diese Nachricht 10 zurückgeben. Dadurch werden Anwendungen angewiesen, 10 Frames vor dem aktuell benötigten Frame zu halten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





