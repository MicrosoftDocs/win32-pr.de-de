---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entladen wird.
title: FMEVENT_UNLOAD Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127864"
---
# <a name="fmevent_unload-message"></a>Meldung zum Entladen des Ereignisses \_

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entladen wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die *HWND* -und **HMENU** -Werte, die mit den " [**fmevent \_ Load**](fmevent-load.md) "-und " [**fmevent \_ InitMenu**](fmevent-initmenu.md) "-Meldungen übergeben werden, sind möglicherweise zum Zeitpunkt der Übermittlung dieser Nachricht ungültig.

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

 

 




