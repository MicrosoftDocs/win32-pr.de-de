---
description: Wird von einer Datei-Manager-Erweiterung gesendet, die bewirkt, dass der Datei-Manager entweder das aktive Fenster oder alle zugehörigen Fenster neu zeichnet.
title: FM_REFRESH_WINDOWS Meldung (WF. h)
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
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214306"
---
# <a name="fm_refresh_windows-message"></a>FM \_ Windows-Aktualisierungs \_ Meldung

Wird von einer Datei-Manager-Erweiterung gesendet, die bewirkt, dass der Datei-Manager entweder das aktive Fenster oder alle zugehörigen Fenster neu zeichnet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*frepaint* 
</dt> <dd>

Ein Wert, der angibt, ob der Datei-Manager das aktive Fenster oder alle zugehörigen Fenster neu zeichnet. Wenn dieser Parameter auf **true** gesetzt ist, zeichnet der Datei-Manager alle zugehörigen Fenster auf. Andernfalls zeichnet der Datei-Manager nur das aktive Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Dateisystem Änderungen, die durch eine Erweiterung verursacht werden, werden automatisch vom Datei-Manager erkannt. Eine Erweiterung sollte diese Nachricht nur in Situationen verwenden, in denen Laufwerk Verbindungen hergestellt oder abgebrochen werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> </dl>

 

 




