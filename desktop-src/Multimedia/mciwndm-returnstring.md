---
title: MCIWNDM_RETURNSTRING Meldung (VFW. h)
description: Die mciwndm- \_ Nachricht "returnstring" Ruft die Antwort auf den aktuellen MCI-Zeichen folgen Befehl ab, der an ein MCI-Gerät gesendet wurde.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING-Nachricht (Multimedia)
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
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040580"
---
# <a name="mciwndm_returnstring-message"></a>Mciwndm- \_ returnstring-Nachricht

Die **mciwndm-Nachricht " \_ returnstring** " Ruft die Antwort auf den aktuellen MCI-Zeichen folgen Befehl ab, der an ein MCI-Gerät gesendet wurde. Die Informationen in der Antwort werden als eine auf NULL endenden Zeichenfolge bereitgestellt. Sie können diese Nachricht explizit oder mithilfe des [**mciwndreturnstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) -Makros senden.


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Nest*
</dt> <dd>

Größe (in Bytes) des Puffers.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ein Zeiger auf einen Anwendungs definierten Puffer, der die auf NULL endenden Zeichenfolge enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der MCI-Zeichenfolge entspricht.

## <a name="remarks"></a>Bemerkungen

Wenn die NULL-terminierte Zeichenfolge länger als der Puffer ist, wird die Zeichenfolge abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndreturnstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





