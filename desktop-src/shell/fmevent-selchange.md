---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Verzeichnisfenster des Datei-Managers oder im Fenster Suchergebnisse auswählt.
title: FMEVENT_SELCHANGE (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: befc217eeb24453d7db726cf68d233fa57e5a7971fd148406cf90810b52b070d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459037"
---
# <a name="fmevent_selchange-message"></a>FMEVENT \_ SELCHANGE-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Verzeichnisfenster des Datei-Managers oder im Fenster Suchergebnisse auswählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn sie diese Meldung verarbeitet.

## <a name="remarks"></a>Hinweise

Änderungen im Strukturbereich des Verzeichnisfensters erzeugen diese Meldung nicht.

Da der Benutzer die Auswahl mehrmals ändern kann, muss die Erweiterungs-DLL nach der Verarbeitung dieser Meldung sofort zurückkehren, um zu vermeiden, dass der Auswahlprozess für den Benutzer verlangsamt wird.

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

 

 




