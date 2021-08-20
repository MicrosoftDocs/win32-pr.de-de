---
title: ICM_DECOMPRESS Nachricht (Vfw.h)
description: Die ICM \_ DECOMPRESS-Nachricht benachrichtigt einen Videodekomprimierungstreiber, um einen Datenrahmen in einen von der Anwendung definierten Puffer zu dekomprimiert.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8285019830820ef9e613c04f07a98d00d11c51982167a0fdd9c8f219853fb175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987900"
---
# <a name="icm_decompress-message"></a>\_ICM DECOMPRESS-Nachricht

Die **ICM \_ DECOMPRESS-Nachricht** benachrichtigt einen Videodekomprimierungstreiber, um einen Frame von Daten in einen von der Anwendung definierten Puffer zu dekomprimiert.


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*Icd*
</dt> <dd>

Zeiger auf eine [**ICDECOMPRESS-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe (in Bytes) von [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Wenn der Treiber Daten direkt auf dem Bildschirm dekomprimieren soll, senden Sie die [**ICM \_ DRAW-Nachricht.**](icm-draw.md)

Der Treiber gibt einen Fehler zurück, wenn diese Meldung vor der [**ICM \_ DECOMPRESS \_ BEGIN-Nachricht**](icm-decompress-begin.md) empfangen wird.

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

 

 





