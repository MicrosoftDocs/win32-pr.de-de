---
title: ICM_COMPRESS_FRAMES_INFO Meldung (VFW. h)
description: In der Info Meldung zum ICM- \_ komprimieren wird \_ \_ ein Komprimierungs Treiber benachrichtigt, um die Parameter für die ausstehende Komprimierung festzulegen.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478465"
---
# <a name="icm_compress_frames_info-message"></a>ICM- \_ Informationen zum Komprimieren von \_ Frames \_

In der **\_ \_ \_ Info Meldung zum ICM-komprimieren** wird ein Komprimierungs Treiber benachrichtigt, um die Parameter für die ausstehende Komprimierung festzulegen.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*ICF*
</dt> <dd>

Zeiger auf eine [**iccompressframes**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) -Struktur. Die **GetData** -und **putdata** -Member dieser Struktur werden mit dieser Nachricht nicht verwendet.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**iccompressframes**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Ein-Kompressor kann diese Meldung verwenden, um zu bestimmen, wie viel Speicherplatz für jeden Frame während der Komprimierung belegt werden soll.

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

 

 





