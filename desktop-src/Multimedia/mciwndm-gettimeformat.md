---
title: MCIWNDM_GETTIMEFORMAT Meldung (VFW. h)
description: Die mciwndm \_ getTimeFormat-Nachricht Ruft das aktuelle Zeitformat eines MCI-Geräts in zwei Formularen als numerischen Wert und als Zeichenfolge ab. Sie können diese Nachricht explizit oder mit dem mciwndgettimeformat-Makro senden.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740240"
---
# <a name="mciwndm_gettimeformat-message"></a>Mciwndm \_ getTimeFormat-Meldung

Die **mciwndm \_ getTimeFormat** -Meldung Ruft das aktuelle Zeitformat eines MCI-Geräts in zwei Formen ab: als numerischer Wert und als Zeichenfolge. Sie können diese Nachricht explizit oder mit dem [**mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) -Makro senden.


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Nest*
</dt> <dd>

Größe (in Bytes) des Puffers.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Zeiger auf einen Puffer, der die NULL-terminierte Zeichen folgen Form des Zeit Formats enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der MCI-Konstante entspricht, die das Zeitformat definiert.

## <a name="remarks"></a>Bemerkungen

Wenn die Zeitformat Zeichenfolge länger als der Rückgabe Puffer ist, wird die Zeichenfolge von mciwnd abgeschnitten.

Ein MCI-Gerät kann eines oder mehrere der folgenden Zeitformate unterstützen.



| Zeitformat                      | MCI-Konstante               |
|----------------------------------|----------------------------|
| Byte                            | MCI- \_ Format ( \_ Bytes)         |
| Frames                           | MCI- \_ Formatierungs \_ Frames        |
| Stunden, Minuten, Sekunden          | MCI- \_ Format \_ HMS           |
| Millisekunden                     | MCI- \_ Format ( \_ Millisekunden)  |
| Minuten, Sekunden, Frames         | MCI- \_ Format \_ MSF           |
| Beispiele                          | MCI- \_ Format \_ Beispiele       |
| SMPTE 24                         | MCI- \_ Format, \_ SMPTE \_ 24     |
| SMPTE 25                         | MCI- \_ Format, \_ SMPTE \_ 25     |
| SMPTE 30-Drop                    | MCI- \_ Format \_ SMPTE \_ 30drop |
| SMPTE 30 (Non-Drop)              | MCI- \_ Format \_ SMPTE \_ 30     |
| Spuren, Minuten, Sekunden, Frames | MCI- \_ Format- \_ TMSF          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





