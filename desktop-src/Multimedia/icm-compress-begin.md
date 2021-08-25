---
title: ICM_COMPRESS_BEGIN (Vfw.h)
description: Die ICM \_ COMPRESS \_ BEGIN-Nachricht benachrichtigt einen Videokomprimierungstreiber, um die Komprimierung von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des ICCompressBegin-Makros senden.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN von Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33a6ee9c080e2dfc7a779abd4ae2a788bbe136ddcab1ef529714639065553ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140948"
---
# <a name="icm_compress_begin-message"></a>\_ICM COMPRESS \_ BEGIN-Nachricht

Die **ICM \_ COMPRESS \_ BEGIN-Nachricht** benachrichtigt einen Videokomprimierungstreiber, um die Komprimierung von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des [**ICCompressBegin-Makros**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) senden.


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) die das Eingabeformat enthält.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) die das Ausgabeformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR OK zurück, wenn der Treiber die angegebene Komprimierung unterstützt, oder ICERR BADFORMAT, wenn das Eingabe- oder \_ \_ Ausgabeformat nicht unterstützt wird.

## <a name="remarks"></a>Hinweise

Der Treiber sollte alle Tabellen oder den Arbeitsspeicher zuordnen und initialisieren, die er zum Komprimieren der Datenformate benötigt, wenn er die ICM [**\_ COMPRESS empfängt.**](icm-compress.md)

VCM speichert die Einstellungen der letzten ICM **\_ COMPRESS \_ BEGIN-Nachricht.** Die **ICM \_ COMPRESS \_ BEGIN-** [**und ICM COMPRESS \_ \_ END-Meldungen**](icm-compress-end.md) werden nicht geschachtelt. Wenn Ihr Treiber ICM **\_ COMPRESS \_ BEGIN** empfängt, bevor die Komprimierung mit ICM COMPRESS **\_ \_ END** beendet wird, sollte die Komprimierung mit neuen Parametern neu gestartet werden.

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

 

