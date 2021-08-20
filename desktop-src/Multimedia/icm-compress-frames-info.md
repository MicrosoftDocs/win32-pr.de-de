---
title: ICM_COMPRESS_FRAMES_INFO Nachricht (Vfw.h)
description: Die \_ ICM COMPRESS \_ FRAMES \_ INFO-Meldung benachrichtigt einen Komprimierungstreiber, die Parameter für die ausstehende Komprimierung festzulegen.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO nachricht Windows Multimedia
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
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140911"
---
# <a name="icm_compress_frames_info-message"></a>\_ICM COMPRESS \_ FRAMES \_ INFO message

Die **ICM COMPRESS FRAMES \_ \_ \_ INFO-Meldung** benachrichtigt einen Komprimierungstreiber, die Parameter für die ausstehende Komprimierung festzulegen.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*Icf*
</dt> <dd>

Zeiger auf eine [**ICCOMPRESSFRAMES-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) Die **Elemente GetData** und **PutData** dieser Struktur werden nicht mit dieser Nachricht verwendet.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe von [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Ein Sprecher kann diese Meldung verwenden, um zu bestimmen, wie viel Speicherplatz für jeden Frame während der Komprimierung belegt werden soll.

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

 

 





