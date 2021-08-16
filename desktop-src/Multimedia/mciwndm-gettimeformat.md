---
title: MCIWNDM_GETTIMEFORMAT Meldung (Vfw.h)
description: Die MCIWNDM \_ GETTIMEFORMAT-Nachricht ruft das aktuelle Zeitformat eines MCI-Geräts in zwei Formen als numerischer Wert und als Zeichenfolge ab. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetTimeFormat-Makros senden.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT nachricht Windows Multimedia
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
ms.openlocfilehash: 3badb7c7722db6444d3bd928535790876e0a128e69e50323cea3fe39c2dd987a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985908"
---
# <a name="mciwndm_gettimeformat-message"></a>MCIWNDM \_ GETTIMEFORMAT-Nachricht

Die **MCIWNDM \_ GETTIMEFORMAT-Nachricht** ruft das aktuelle Zeitformat eines MCI-Geräts in zwei Formen ab: als numerischer Wert und als Zeichenfolge. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetTimeFormat-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) senden.


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Größe des Puffers in Bytes.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf einen Puffer, der die auf NULL endende Zeichenfolgenform des Zeitformats enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der MCI-Konstante entspricht, die das Zeitformat definiert.

## <a name="remarks"></a>Hinweise

Wenn die Zeitformatzeichenfolge länger als der Rückgabepuffer ist, schneidet MCIWnd die Zeichenfolge ab.

Ein MCI-Gerät kann eines oder mehrere der folgenden Zeitformate unterstützen.



| Zeitformat                      | MCI-Konstante               |
|----------------------------------|----------------------------|
| Byte                            | \_MCI-FORMAT \_ BYTE         |
| Frames                           | \_ \_ MCI-FORMATFRAMES        |
| Stunden, Minuten, Sekunden          | MCI \_ FORMAT \_ HMS           |
| Millisekunden                     | \_MCI-FORMAT \_ MILLISEKUNDEN  |
| Minuten, Sekunden, Frames         | MCI \_ FORMAT \_ MSF           |
| Beispiele                          | \_ \_ MCI-FORMATBEISPIELE       |
| SMPTE 24                         | MCI \_ FORMAT \_ SMPTE \_ 24     |
| SMPTE 25                         | MCI \_ FORMAT \_ SMPTE \_ 25     |
| SMPTE 30-Ablage                    | MCI \_ FORMAT \_ SMPTE \_ 30DROP |
| SMPTE 30 (ohne Ablage)              | MCI \_ FORMAT \_ SMPTE \_ 30     |
| Spuren, Minuten, Sekunden, Frames | MCI \_ FORMAT \_ TMSF          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





