---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnis Fenster oder im Fenster "Suchergebnisse" auswählt.
title: FMEVENT_SELCHANGE Meldung (WF. h)
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
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524504"
---
# <a name="fmevent_selchange-message"></a>\_Meldung zum Ändern der Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnis Fenster oder im Fenster "Suchergebnisse" auswählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nicht durch Änderungen im Strukturbereich des Verzeichnis Fensters erzeugt.

Da der Benutzer die Auswahl mehrmals ändern kann, muss die Erweiterungs-DLL nach der Verarbeitung dieser Nachricht umgehend zurückgeben, um zu vermeiden, dass der Auswahl Vorgang für den Benutzer verlangsamt wird.

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

 

 




