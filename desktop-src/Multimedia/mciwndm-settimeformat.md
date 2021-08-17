---
title: MCIWNDM_SETTIMEFORMAT (Vfw.h)
description: Die MCIWNDM-Nachricht \_ SETTIMEFORMAT legt das Zeitformat eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndSetTimeFormat senden.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT von Windows Multimedia
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
ms.openlocfilehash: 79620aecba07b11ed63dfc43fd2d70b41728586b36649b4b13aace9d1364197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802894"
---
# <a name="mciwndm_settimeformat-message"></a>MCIWNDM \_ SETTIMEFORMAT-Meldung

Die **MCIWNDM-Nachricht \_ SETTIMEFORMAT legt** das Zeitformat eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) senden.


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf einen Puffer, der die auf NULL beendete Zeichenfolge enthält, die das Zeitformat angibt. Geben Sie "Frames" an, um das Zeitformat auf Frames festzulegen, oder "ms", um das Zeitformat auf Millisekunden festzulegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Eine Anwendung kann andere Zeitformate als Frames oder Millisekunden angeben, solange die Formate vom MCI-Gerät unterstützt werden. Nicht nebenkontinuierliche Formate wie Tracks und SMPTE können dazu führen, dass sich die Trackleiste unanständlich verhält. Für diese Zeitformate können Sie die Symbolleiste mithilfe des [**MCIWndChangeStyles-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) deaktivieren und den MCIWNDF \_ NOPLAYBAR-Fensterstil angeben.

Wenn Sie das Zeitformat auf Frames oder Millisekunden festlegen möchten, können Sie auch das [**Makro MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) oder [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) verwenden. Eine Liste der Zeitformate finden Sie im [**MCIWndGetTimeFormat-Makro.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





