---
title: ICM_DECOMPRESS Meldung (VFW. h)
description: Die ICM \_ dekomprimieren-Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um einen Datenrahmen in einen Anwendungs definierten Puffer zu dekomprimieren.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS-Nachricht (Multimedia)
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
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040878"
---
# <a name="icm_decompress-message"></a>ICM- \_ Dekomprimierungs Meldung

Die **ICM \_ dekomprimieren** -Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um einen Datenrahmen in einen Anwendungs definierten Puffer zu dekomprimieren.


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*ICD*
</dt> <dd>

Zeiger auf eine [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) -Struktur.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw**](icm-draw.md) -Nachricht.

Der Treiber gibt einen Fehler zurück, wenn diese Nachricht vor der [**ICM- \_ Dekomprimierungs \_ Begin**](icm-decompress-begin.md) -Nachricht empfangen wird.

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

 

 





