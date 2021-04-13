---
title: ICM_COMPRESS_GET_FORMAT Meldung (VFW. h)
description: Die ICM \_ Compress \_ get \_ Format-Meldung fordert das Ausgabeformat der komprimierten Daten von einem Video Komprimierungs Treiber an. Sie können diese Nachricht explizit oder mithilfe des iccompressgetformat-Makros senden.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478468"
---
# <a name="icm_compress_get_format-message"></a>ICM \_ Compress \_ - \_ Format Meldung "Get"

Die **ICM \_ Compress \_ get \_ Format** -Meldung fordert das Ausgabeformat der komprimierten Daten von einem Video Komprimierungs Treiber an. Sie können diese Nachricht explizit oder mithilfe des [**iccompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) -Makros senden.


```C++
ICM_COMPRESS_GET_FORMAT 
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

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthalten soll. Sie können NULL für diesen Parameter angeben, um nur die Größe des Ausgabeformats anzufordern, wie im " [**iccompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) "-Makro.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn *lpbioutput* gleich 0 (null) ist, wird die Größe der Struktur zurückgegeben.

Wenn *lpbioutput* ungleich NULL ist, gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Wenn *lpbioutput* ungleich NULL ist, sollte der Treiber die [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur mit dem Standardausgabeformat auffüllen, das dem für *lpbiinput* angegebenen Eingabeformat entspricht. Wenn der-Kompressor mehrere Formate liefern kann, sollte das Standardformat das Standardformat aufweisen, das die größte Menge an Informationen beibehält.

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

 

