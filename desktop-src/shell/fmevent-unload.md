---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entlädt.
title: FMEVENT_UNLOAD (Wfext.h)
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
ms.openlocfilehash: 5d18d72a43ac1fca6906bb1e3f7a14468dbd02933d801dc3c20e2a933bc18f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860365"
---
# <a name="fmevent_unload-message"></a>FMEVENT \_ UNLOAD-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entlädt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn sie diese Meldung verarbeitet.

## <a name="remarks"></a>Hinweise

Die *hwnd-* und **hMenu-Werte,** die mit [**den FMEVENT \_ LOAD-**](fmevent-load.md) und [**FMEVENT \_ INITMENU-Nachrichten**](fmevent-initmenu.md) übergeben werden, sind möglicherweise zum Zeitpunkt des Sendens dieser Nachricht ungültig.

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

 

 




