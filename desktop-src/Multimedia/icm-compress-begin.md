---
title: ICM_COMPRESS_BEGIN Meldung (VFW. h)
description: Mit der ICM- \_ Komprimierungs \_ Begin-Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Komprimieren von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des iccompressbegin-Makros senden.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040988"
---
# <a name="icm_compress_begin-message"></a>ICM- \_ Komprimierungs \_ Begin-Meldung

Mit der **ICM- \_ Komprimierungs \_ Begin** -Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Komprimieren von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des [**iccompressbegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) -Makros senden.


```C++
ICM_COMPRESS_BEGIN 
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

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber die angegebene Komprimierung oder ICERR badformat unterstützt, \_ Wenn das Eingabe-oder Ausgabeformat nicht unterstützt wird.

## <a name="remarks"></a>Bemerkungen

Der Treiber sollte alle Tabellen oder Arbeitsspeicher zuweisen und initialisieren, die er zum Komprimieren der Datenformate benötigt, wenn er die [**ICM- \_ Komprimierungs**](icm-compress.md) Nachricht empfängt.

VCM speichert die Einstellungen der letzten **ICM- \_ Komprimierungs \_ Begin** -Nachricht. Die **ICM- \_ Komprimierungs \_ Begin** -und [**ICM- \_ Komprimierungs \_**](icm-compress-end.md) Meldungen werden nicht geschachtelt. Wenn der Treiber **ICM \_ Compress \_ Begin** empfängt, bevor die Komprimierung mit **ICM- \_ Komprimierung \_ beendet** wird, sollte die Komprimierung mit neuen Parametern neu gestartet werden.

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

 

