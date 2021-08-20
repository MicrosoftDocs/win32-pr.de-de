---
title: MCIWNDM_GETERROR (Vfw.h)
description: Die MCIWNDM \_ GETERROR-Meldung ruft den letzten gefundenen MCI-Fehler ab. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetError-Makros senden.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b748aec6cf686ecf47baf8deae621514e620971f5e1da667f8e4f0aae708ab80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137721"
---
# <a name="mciwndm_geterror-message"></a>MCIWNDM \_ GETERROR-Meldung

Die **MCIWNDM \_ GETERROR-Meldung** ruft den letzten gefundenen MCI-Fehler ab. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetError-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) senden.


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Größe des Fehlerpuffers in Bytes.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf einen anwendungsdefinierten Puffer, der zum Zurückgeben der Fehlerzeichenfolge verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den ganzzahligen Fehlerwert zurück.

## <a name="remarks"></a>Hinweise

Wenn *lp* ein gültiger Zeiger ist, wird eine auf NULL beendete Zeichenfolge, die dem Fehler entspricht, im Puffer zurückgegeben. Wenn die Fehlerzeichenfolge länger als der Puffer ist, wird sie von MCIWnd abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





