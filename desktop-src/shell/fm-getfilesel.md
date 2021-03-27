---
description: Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse").
title: FM_GETFILESEL Meldung (WF. h)
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
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864947"
---
# <a name="fm_getfilesel-message"></a>FM \_ getfilesel-Meldung

Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse").

## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Der null basierte Index der ausgewählten Datei, die abgerufen werden soll.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Die Adresse einer [**f- \_ getfilesel**](fms-getfilesel.md) -Struktur, die Informationen über die Auswahl empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den NULL basierten Index der ausgewählten Datei zurück, die abgerufen wurde.

## <a name="remarks"></a>Bemerkungen

Eine Erweiterung kann die [**FM \_ getselcount**](fm-getselcount.md) -Nachricht verwenden, um die Anzahl ausgewählter Dateien abzurufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> <dt>

[**FM \_ getfilesellfn**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ getselzähltlfn**](fm-getselcountlfn.md)
</dt> </dl>

 

 




