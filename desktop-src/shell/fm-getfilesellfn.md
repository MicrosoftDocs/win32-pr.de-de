---
description: Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse"). Die ausgewählte Datei kann einen langen Dateinamen haben.
title: FM_GETFILESELLFN Meldung (WF. h)
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
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484046"
---
# <a name="fm_getfilesellfn-message"></a>FM \_ getfilesellfn-Nachricht

Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse"). Die ausgewählte Datei kann einen langen Dateinamen haben.

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

Diese Nachricht sollte nur von Erweiterungen verwendet werden, die lange Dateinamen unterstützen (z. b. Netzwerk abhängige Erweiterungen).

Eine Erweiterung kann die [**FM \_ getselzähltlfn**](fm-getselcountlfn.md) -Nachricht verwenden, um die Anzahl ausgewählter Dateien abzurufen.

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

[**FM \_ getfilesel**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ getselcount**](fm-getselcount.md)
</dt> </dl>

 

 




