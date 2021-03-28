---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerks Informationen aus dem aktiven Datei-Manager-Fenster abzurufen.
title: FM_GETDRIVEINFO Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993703"
---
# <a name="fm_getdriveinfo-message"></a>FM \_ GetDriveInfo-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerks Informationen aus dem aktiven Datei-Manager-Fenster abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Die Adresse einer [**FMS \_ GetDriveInfo**](fms-getdriveinfo.md) -Struktur, die Laufwerk Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 zurück.

## <a name="remarks"></a>Bemerkungen

Wenn 0xFFFFFFFF im **dwtotalspace** -oder **dwfreespace** -Member der [**FMS \_ GetDriveInfo**](fms-getdriveinfo.md) -Struktur zurückgegeben wird, muss die Erweiterungs Bibliothek den Wert oder die Werte berechnen.

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

 

 




