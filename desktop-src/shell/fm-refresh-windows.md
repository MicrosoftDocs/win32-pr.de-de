---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um zu bewirken, dass der Datei-Manager entweder das aktive Fenster oder alle Fenster neu malt.
title: FM_REFRESH_WINDOWS Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842351"
---
# <a name="fm_refresh_windows-message"></a>FM \_ REFRESH \_ WINDOWS-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, damit der Datei-Manager entweder das aktive Fenster oder alle Fenster neu malt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*fRepaint* 
</dt> <dd>

Ein -Wert, der angibt, ob der Datei-Manager das aktive Fenster oder alle Fenster neu malt. Wenn dieser Parameter **TRUE** ist, zeichnet der Datei-Manager alle Fenster neu. Andernfalls bemalt der Datei-Manager nur das aktive Fenster neu.

</dd> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Dateisystemänderungen, die durch eine Erweiterung verursacht werden, werden automatisch vom Datei-Manager erkannt. Eine Erweiterung sollte diese Meldung nur in Situationen verwenden, in denen Laufwerkverbindungen hergestellt oder abgebrochen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




