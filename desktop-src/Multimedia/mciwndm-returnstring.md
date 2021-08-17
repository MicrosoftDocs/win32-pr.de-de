---
title: MCIWNDM_RETURNSTRING (Vfw.h)
description: Die Meldung MCIWNDM RETURNSTRING ruft die Antwort auf den letzten MCI-Zeichenfolgenbefehl ab, \_ der an ein MCI-Gerät gesendet wurde.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ea9624c70245c67f0f6a78af68bf291ae3ce60ba65ae2cd273008bbc914ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137657"
---
# <a name="mciwndm_returnstring-message"></a>MCIWNDM \_ RETURNSTRING-Meldung

Die **Meldung MCIWNDM \_ RETURNSTRING ruft** die Antwort auf den letzten MCI-Zeichenfolgenbefehl ab, der an ein MCI-Gerät gesendet wurde. Informationen in der Antwort werden als auf NULL beendete Zeichenfolge bereitgestellt. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) senden.


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Größe des Puffers in Bytes.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf einen anwendungsdefinierten Puffer, der die auf NULL beendete Zeichenfolge enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der MCI-Zeichenfolge entspricht.

## <a name="remarks"></a>Hinweise

Wenn die auf NULL terminierte Zeichenfolge länger als der Puffer ist, wird die Zeichenfolge abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





