---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen.
title: FM_GETSELCOUNT Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: aac7d08de3785bb02c31dabc1ef7a25fea0d5b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993702"
---
# <a name="fm_getselcount-message"></a>FM \_ getselcount-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der ausgewählten Dateien zurück.

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

[**FM \_ getselzähltlfn**](fm-getselcountlfn.md)
</dt> </dl>

 

 




