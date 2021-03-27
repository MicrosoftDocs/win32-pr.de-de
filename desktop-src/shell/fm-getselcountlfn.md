---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen. Die Anzahl umfasst Dateien mit langen Dateinamen.
title: FM_GETSELCOUNTLFN Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994758"
---
# <a name="fm_getselcountlfn-message"></a>FM \_ getselzähltlfn-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen. Die Anzahl umfasst Dateien mit langen Dateinamen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der ausgewählten Dateien zurück.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht sollte nur von Erweiterungen verwendet werden, die lange Dateinamen unterstützen (z. b. Netzwerk abhängige Erweiterungen).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FM \_ getfilesel**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ getfilesellfn**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ getselcount**](fm-getselcount.md)
</dt> </dl>

 

 




