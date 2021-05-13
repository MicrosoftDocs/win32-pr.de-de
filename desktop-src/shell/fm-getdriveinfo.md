---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerksinformationen aus dem aktiven Datei-Manager-Fenster abzurufen.
title: FM_GETDRIVEINFO (Wfext.h)
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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842411"
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

Wenn 0xFFFFFFFF **dwTotalSpace-** oder **dwFreeSpace-Member** der [**FMS \_ GETDRIVEINFO-Struktur**](fms-getdriveinfo.md) zurückgegeben wird, muss die Erweiterungsbibliothek den Wert oder die Werte berechnen.

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

 

 




