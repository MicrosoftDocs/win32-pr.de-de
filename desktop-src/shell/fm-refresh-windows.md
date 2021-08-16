---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um zu bewirken, dass der Datei-Manager entweder sein aktives Fenster oder alle seine Fenster neu anpaint.
title: FM_REFRESH_WINDOWS (Wfext.h)
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
ms.openlocfilehash: fa38b55fdcd7c338102ed62bd9d7011ca4b7caf79fa81e834bcf915d8f934464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224266"
---
# <a name="fm_refresh_windows-message"></a>FM \_ REFRESH \_ WINDOWS-Meldung

Wird von einer Datei-Manager-Erweiterung gesendet, um zu bewirken, dass der Datei-Manager entweder sein aktives Fenster oder alle seine Fenster neu anpaint.

## <a name="parameters"></a>Parameter

<dl> <dt>

*fRepaint* 
</dt> <dd>

Ein -Wert, der angibt, ob der Datei-Manager sein aktives Fenster oder alle fenster neu gepaint. Wenn dieser Parameter **TRUE ist,** werden alle Fenster im Datei-Manager neu gepaint. Andernfalls wird vom Datei-Manager nur das aktive Fenster neu gepaint.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




