---
title: MCIWNDM_GETPOSITION Meldung (VFW. h)
description: Die mciwndm \_ GetPosition-Nachricht Ruft den numerischen Wert der aktuellen Position im Inhalt des MCI-Geräts ab.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION-Nachricht (Multimedia)
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
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858704"
---
# <a name="mciwndm_getposition-message"></a>Mciwndm \_ GetPosition-Nachricht

Die **mciwndm \_ GetPosition** -Nachricht Ruft den numerischen Wert der aktuellen Position im Inhalt des MCI-Geräts ab. Dieses Makro stellt außerdem die aktuelle Position in der Zeichenfolge in einem von der Anwendung definierten Puffer bereit. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetposition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) oder [**mciwndgetpositionstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) senden.


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Nest*
</dt> <dd>

Größe (in Bytes) des Puffers. Wenn die auf NULL endenden Zeichenfolge länger als der Puffer ist, wird Sie abgeschnitten. Verwenden Sie 0 (null), um das Abrufen der Position als Zeichenfolge zu verhindern.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Zeiger auf einen Anwendungs definierten Puffer, der zum Zurückgeben der Position verwendet wird. Verwenden Sie 0 (null), um das Abrufen der Position als Zeichenfolge zu verhindern. Wenn das Gerät Spuren unterstützt, werden die Zeichen folgen Positionsinformationen im Format TT: mm: SS: FF zurückgegeben, wobei TT den Titeln entspricht, mm und SS den Minuten und Sekunden entsprechen und FF den Frames entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der aktuellen Position entspricht. Die Einheiten für den Positionswert hängen vom aktuellen Zeitformat ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetposition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**Mciwndgetpositionstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





