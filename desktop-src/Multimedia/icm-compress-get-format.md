---
title: ICM_COMPRESS_GET_FORMAT (Vfw.h)
description: Die ICM COMPRESS GET FORMAT fordert das Ausgabeformat der komprimierten Daten \_ \_ von einem \_ Videokomprimierungstreiber an. Sie können diese Nachricht explizit oder mithilfe des Makros ICCompressGetFormat senden.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac1bf9b3c9a3ae0535da008786bf8baef19c8b51e27446b84e4b95805a1c4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785030"
---
# <a name="icm_compress_get_format-message"></a>\_ICM COMPRESS \_ GET \_ FORMAT-Nachricht

Die **ICM COMPRESS GET \_ \_ \_ FORMAT-Nachricht** fordert das Ausgabeformat der komprimierten Daten von einem Videokomprimierungstreiber an. Sie können diese Nachricht explizit oder mithilfe des [**Makros ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) senden.


```C++
ICM_COMPRESS_GET_FORMAT 
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

Zeiger auf eine [**BITMAPINFO-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) die das Ausgabeformat enthalten soll. Sie können null angeben, damit dieser Parameter nur die Größe des Ausgabeformats angibt, wie im [**ICCompressGetFormatSize-Makro.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn *lpbiOutput* 0 (null) ist, gibt die Größe der -Struktur zurück.

Wenn *lpbiOutput* ungleich 0 (null) ist, gibt ICERR OK zurück, wenn \_ erfolgreich, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Wenn *lpbiOutput* ungleich null ist, sollte der Treiber die [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) mit dem Standardausgabeformat füllen, das dem für *lpbiInput angegebenen Eingabeformat entspricht.* Wenn die Komprimierung mehrere Formate erzeugen kann, sollte das Standardformat das Format sein, das die größte Menge an Informationen beibwahrt.

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

 

