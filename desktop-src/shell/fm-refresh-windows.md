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
ms.openlocfilehash: fa38b55fdcd7c338102ed62bd9d7011ca4b7caf79fa81e834bcf915d8f934464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224266"
---
# <a name="fm_refresh_windows-message"></a>FM \_ REFRESH \_ WINDOWS-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um zu bewirken, dass der Datei-Manager entweder das aktive Fenster oder alle Fenster neu malt.

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

Dateisystemänderungen, die durch eine Erweiterung verursacht werden, werden automatisch vom Datei-Manager erkannt. Eine Erweiterung sollte diese Nachricht nur in Situationen verwenden, in denen Laufwerkverbindungen hergestellt oder abgebrochen werden.

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

 

 




