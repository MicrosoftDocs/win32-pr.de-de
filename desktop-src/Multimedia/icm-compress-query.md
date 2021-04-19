---
title: ICM_COMPRESS_QUERY Meldung (VFW. h)
description: Die ICM \_ - \_ Abfrage Nachricht zum Komprimieren fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat komprimiert werden kann.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- ICM_COMPRESS_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346747"
---
# <a name="icm_compress_query-message"></a>ICM \_ - \_ Abfrage Nachricht komprimieren

Die **ICM \_ - \_ Abfrage** Nachricht zum Komprimieren fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat komprimiert werden kann. Sie können diese Nachricht explizit oder mithilfe des [**iccompressquery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) -Makros senden.


```C++
ICM_COMPRESS_QUERY 
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

Gibt ICERR \_ OK zurück, wenn die angegebene Komprimierung unterstützt wird, andernfalls wird ICERR \_ badformat zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn ein Treiber diese Nachricht empfängt, sollte er die mit " *lpbiinput* " verknüpfte [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur untersuchen, um zu bestimmen, ob er das Eingabeformat komprimieren kann.

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

 

