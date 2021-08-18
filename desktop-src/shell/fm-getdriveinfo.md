---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerksinformationen aus dem aktiven Datei-Manager-Fenster abzurufen.
title: FM_GETDRIVEINFO Nachricht (Wfext.h)
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
ms.openlocfilehash: 39df15a4522e863fada40d3c964d709f40d2a26d01240aaefe51b09924b8c9ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459120"
---
# <a name="fm_getdriveinfo-message"></a>FM \_ GETDRIVEINFO-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerksinformationen aus dem aktiven Datei-Manager-Fenster abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Die Adresse einer [**FMS \_ GETDRIVEINFO-Struktur,**](fms-getdriveinfo.md) die Laufwerkinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Wenn 0xFFFFFFFF im **dwTotalSpace-** oder **dwFreeSpace-Member** der [**FMS \_ GETDRIVEINFO-Struktur**](fms-getdriveinfo.md) zurückgegeben wird, muss die Erweiterungsbibliothek den Wert oder die Werte berechnen.

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

 

 




