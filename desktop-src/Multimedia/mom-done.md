---
title: MOM_DONE-Nachricht (Mciapi.h)
description: Die MOM DONE-Nachricht wird an eine RÜCKRUFFUNKTION für die \_ AUSGABE GESENDET, wenn der angegebene systemausgebundene Puffer oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4361ef25af7bab629138d4371c852d661373891e9d9513ae30b8ad79e97670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807030"
---
# <a name="mom_done-message"></a>MOM \_ DONE-Nachricht

Die **MOM \_ DONE-Nachricht** wird an eine RÜCKRUFFUNKTION für die AUSGABE GESENDET, wenn der angegebene systemausgebundene Puffer oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Zeiger auf eine [**CURSORHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) die den Puffer identifiziert.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserviert; nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

