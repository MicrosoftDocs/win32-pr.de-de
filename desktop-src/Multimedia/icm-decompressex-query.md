---
title: ICM_DECOMPRESSEX_QUERY Meldung (VFW. h)
description: Die ICM \_ decompressex- \_ Abfrage Nachricht fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- ICM_DECOMPRESSEX_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859142"
---
# <a name="icm_decompressex_query-message"></a>ICM- \_ decompressex- \_ Abfrage Nachricht

Die **ICM \_ decompressex- \_ Abfrage** Nachricht fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Zeiger auf eine [**icdecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur, die das Eingabeformat enthält.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)(in Bytes).

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

 

 





