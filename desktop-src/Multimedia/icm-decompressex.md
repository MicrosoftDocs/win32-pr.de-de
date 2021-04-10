---
title: ICM_DECOMPRESSEX Meldung (VFW. h)
description: Durch die ICM \_ decompressex-Nachricht wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen direkt auf dem Bildschirm zu dekomprimieren, auf ein aufwärts Bild aufgeschalteter DIB zu dekomprimieren oder mit Quell-und Ziel Rechtecke beschriebene Bilder zu dekomprimieren.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040877"
---
# <a name="icm_decompressex-message"></a>ICM- \_ decompressex-Nachricht

Durch die **ICM \_ decompressex** -Nachricht wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen direkt auf dem Bildschirm zu dekomprimieren, auf ein aufwärts Bild aufgeschalteter DIB zu dekomprimieren oder mit Quell-und Ziel Rechtecke beschriebene Bilder zu dekomprimieren.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Zeiger auf eine [**icbecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ähnelt [**ICM \_ Decompress**](icm-decompress.md) , mit dem Unterschied, dass Sie die [**icdecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur verwendet, um die dekomprimierungsinformationen zu definieren.

Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw**](icm-draw.md) -Nachricht.

Der Treiber gibt einen Fehler zurück, wenn diese Nachricht vor der [**ICM- \_ decompressex- \_ Begin**](icm-decompressex-begin.md) -Nachricht empfangen wird.

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

 

 





