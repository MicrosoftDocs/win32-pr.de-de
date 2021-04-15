---
title: MCIWNDM_SETTIMEFORMAT Meldung (VFW. h)
description: Die mciwndm- \_ settimeformat-Meldung legt das Zeitformat eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mit dem mciwndsettimeformat-Makro senden.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517414"
---
# <a name="mciwndm_settimeformat-message"></a>Mciwndm- \_ settimeformat-Meldung

Die **mciwndm- \_ settimeformat** -Meldung legt das Zeitformat eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mit dem [**mciwndsettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) -Makro senden.


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Zeiger auf einen Puffer, der die NULL-terminierte Zeichenfolge enthält, die das Zeitformat angibt. Geben Sie "Frames" an, um das Zeitformat auf Frames festzulegen, oder "MS", um das Zeitformat auf Millisekunden festzulegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

In einer Anwendung können andere Zeitformate als Frames oder Millisekunden angegeben werden, solange die Formate vom MCI-Gerät unterstützt werden. Nicht kontinuierliche Formate, wie z. b. "Tracks" und "SMPTE", können dazu führen, dass sich die TrackBar in der Status- Für diese Zeitformate empfiehlt es sich, die Symbolleiste zu deaktivieren, indem Sie das [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makro verwenden und den Fenster Stil mciwndf \_ noplaybar angeben.

Wenn Sie das Zeitformat auf Frames oder Millisekunden festlegen möchten, können Sie auch das Makro [**mciwnduseframes**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) oder [**mciwndusetime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) verwenden. Eine Liste der Zeitformate finden Sie unter dem [**mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) -Makro.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**Mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**Mciwndsettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**Mciwnduabframes**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**Mciwndul-Zeit**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





