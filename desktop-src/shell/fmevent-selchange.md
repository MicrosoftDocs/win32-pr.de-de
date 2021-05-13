---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnisfenster oder im Fenster Suchergebnisse auswählt.
title: FMEVENT_SELCHANGE Nachricht (Wfext.h)
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
ms.openlocfilehash: e9aa647434aab5a483626757179a7b23b3372a02
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842261"
---
# <a name="fmevent_selchange-message"></a>FMEVENT \_ SELCHANGE-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnisfenster oder im Fenster Suchergebnisse auswählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.

## <a name="remarks"></a>Hinweise

Änderungen am Strukturteil des Verzeichnisfensters erzeugen diese Meldung nicht.

Da der Benutzer die Auswahl mehrmals ändern kann, muss die Erweiterungs-DLL nach der Verarbeitung dieser Meldung sofort zurückgeben, um eine Verlangsamung des Auswahlprozesses für den Benutzer zu vermeiden.

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

 

 




