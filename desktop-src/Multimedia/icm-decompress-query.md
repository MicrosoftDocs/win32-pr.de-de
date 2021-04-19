---
title: ICM_DECOMPRESS_QUERY Meldung (VFW. h)
description: Die ICM \_ dekomprimieren- \_ Abfrage Nachricht fragt einen Video Dekomprimierung-Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342867"
---
# <a name="icm_decompress_query-message"></a>ICM- \_ \_ Abfrage Nachricht dekomprimieren

Die **ICM \_ dekomprimieren- \_ Abfrage** Nachricht fragt einen Video Dekomprimierung-Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann. Sie können diese Nachricht explizit oder mithilfe des [**icdecompressquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) -Makros senden.


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält. Sie können NULL für diesen Parameter angeben, um anzugeben, dass ein beliebiges Ausgabeformat zulässig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.

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

 

