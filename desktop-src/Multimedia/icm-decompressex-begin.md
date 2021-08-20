---
title: ICM_DECOMPRESSEX_BEGIN (Vfw.h)
description: Die ICM DECOMPRESSEX BEGIN-Nachricht benachrichtigt einen Videokomprimierungstreiber, um die Dekomprimierung \_ \_ von Daten vorzubereiten.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc74d5573437a1606db89377e36442b51677aca016cebd9635a0ab4f64cc55e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987812"
---
# <a name="icm_decompressex_begin-message"></a>\_ICM DECOMPRESSEX \_ BEGIN-Meldung

Die **ICM \_ DECOMPRESSEX \_ BEGIN-Nachricht** benachrichtigt einen Videokomprimierungstreiber, um die Dekomprimierung von Daten vorzubereiten.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Zeiger auf eine [**ICDECOMPRESSEX-Struktur,**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) die die Eingabe- und Ausgabeformate enthält.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe von [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird, andernfalls ICERR \_ BADFORMAT.

## <a name="remarks"></a>Hinweise

Wenn der Treiber diese Nachricht empfängt, sollte er Puffer zuordnen und zeitaufwändige Vorgänge für die effiziente Verarbeitung ICM [**\_ DECOMPRESSEX-Nachrichten**](icm-decompressex.md) erledigen.

Wenn der Treiber Daten direkt auf dem Bildschirm dekomprimieren soll, senden Sie die ICM [**\_ DRAW \_ BEGIN-Nachricht.**](icm-draw-begin.md)

Die **ICM \_ DECOMPRESSEX \_ BEGIN-** [**und ICM \_ DECOMPRESSEX \_ END-Meldungen**](icm-decompressex-end.md) werden nicht geschachtelt. Wenn Ihr Treiber ICM **\_ DECOMPRESSEX \_ BEGIN** empfängt, bevor die Dekomprimierung mit **ICM \_ DECOMPRESSEX \_ END** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





