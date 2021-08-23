---
title: ICM_COMPRESS Nachricht (Vfw.h)
description: Die ICM \_ COMPRESS-Nachricht benachrichtigt einen Videokomprimierungstreiber, einen Frame von Daten in einen von der Anwendung definierten Puffer zu komprimieren.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678470"
---
# <a name="icm_compress-message"></a>\_ICM COMPRESS-Nachricht

Die **ICM \_ COMPRESS-Nachricht** benachrichtigt einen Videokomprimierungstreiber, einen Frame von Daten in einen von der Anwendung definierten Puffer zu komprimieren.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*Icc*
</dt> <dd>

Zeiger auf eine [**ICCOMPRESS-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-iccompress) Die folgenden Member dieser Struktur geben die Komprimierungsparameter an: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lplimitd**, **lpdwFlags**, **dwFrameSize** und **dwQuality**. Der Treiber sollte auch den **biSizeImage-Member** der [**BITMAPINFOHEADER-Struktur**](/previous-versions//dd183376(v=vs.85)) verwenden, die **lpbiOutput** von **ICCOMPRESS** zugeordnet ist, um die Größe des komprimierten Frames zurückzugeben.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe (in Bytes) von [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, oder andernfalls ein Fehler.

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

 

