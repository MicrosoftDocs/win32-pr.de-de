---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse). Die ausgewählte Datei kann einen langen Dateinamen haben.
title: FM_GETFILESELLFN (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842391"
---
# <a name="fm_getfilesellfn-message"></a>FM \_ GETFILESELLFN-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse). Die ausgewählte Datei kann einen langen Dateinamen haben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Der nullbasierte Index der abzurufenden ausgewählten Datei.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Die Adresse einer [**FMS \_ GETFILESEL-Struktur,**](fms-getfilesel.md) die Informationen zur Auswahl empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den nullbasierten Index der ausgewählten Datei zurück, die abgerufen wurde.

## <a name="remarks"></a>Hinweise

Nur Erweiterungen, die lange Dateinamen unterstützen (z. B. netzwerkspezifische Erweiterungen), sollten diese Meldung verwenden.

Eine Erweiterung kann die [**FM \_ GETSELCOUNTLFN-Nachricht**](fm-getselcountlfn.md) verwenden, um die Anzahl der ausgewählten Dateien abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




