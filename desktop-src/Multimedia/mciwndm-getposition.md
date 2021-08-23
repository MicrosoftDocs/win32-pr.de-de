---
title: MCIWNDM_GETPOSITION Meldung (Vfw.h)
description: Die MCIWNDM \_ GETPOSITION-Nachricht ruft den numerischen Wert der aktuellen Position im Inhalt des MCI-Geräts ab.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83cf16f5945bfccbfd2f745ba22fac750f0536696aa2c4c06c2872bd318b263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525430"
---
# <a name="mciwndm_getposition-message"></a>MCIWNDM \_ GETPOSITION-Nachricht

Die **MCIWNDM \_ GETPOSITION-Nachricht** ruft den numerischen Wert der aktuellen Position im Inhalt des MCI-Geräts ab. Dieses Makro stellt auch die aktuelle Position in Zeichenfolgenform in einem anwendungsdefiniertem Puffer bereit. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetPosition-**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) oder [**MCIWndGetPositionString-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) senden.


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Größe des Puffers in Bytes. Wenn die auf NULL endende Zeichenfolge länger als der Puffer ist, wird sie abgeschnitten. Verwenden Sie 0 (null), um den Abruf der Position als Zeichenfolge zu verhindern.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf einen anwendungsdefinierte Puffer, der verwendet wird, um die Position zurückzugeben. Verwenden Sie 0 (null), um den Abruf der Position als Zeichenfolge zu verhindern. Wenn das Gerät Spuren unterstützt, werden die Informationen zur Zeichenfolgenposition in der Form TT:MM:SS:FF zurückgegeben, wobei TT Spuren entspricht, MM und SS Minuten und Sekunden entsprechen und FF Frames entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der aktuellen Position entspricht. Die Einheiten für den Positionswert hängen vom aktuellen Zeitformat ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





