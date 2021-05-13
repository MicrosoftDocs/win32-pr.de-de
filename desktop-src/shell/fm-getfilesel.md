---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse).
title: FM_GETFILESEL Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841421"
---
# <a name="fm_getfilesel-message"></a>FM \_ GETFILESEL-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse).

## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Der nullbasierte Index der ausgewählten abzurufenden Datei.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Die Adresse einer [**FMS \_ GETFILESEL-Struktur,**](fms-getfilesel.md) die Informationen zur Auswahl empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den nullbasierten Index der ausgewählten Datei zurück, die abgerufen wurde.

## <a name="remarks"></a>Hinweise

Eine Erweiterung kann die [**FM \_ GETSELCOUNT-Nachricht**](fm-getselcount.md) verwenden, um die Anzahl der ausgewählten Dateien abzurufen.

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

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md)
</dt> </dl>

 

 




