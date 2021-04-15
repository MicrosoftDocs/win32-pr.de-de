---
title: MCIWNDM_GETFILENAME Meldung (VFW. h)
description: Die mciwndm \_ GetFileName-Nachricht Ruft den Dateinamen ab, der derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mit dem mciwndgetfilename-Makro senden.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- MCIWNDM_GETFILENAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517426"
---
# <a name="mciwndm_getfilename-message"></a>Mciwndm \_ GetFileName-Meldung

Die **mciwndm \_ GetFileName** -Nachricht Ruft den Dateinamen ab, der derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mit dem [**mciwndgetfilename**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) -Makro senden.


```C++
MCIWNDM_GETFILENAME 
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

Zeiger auf einen Anwendungs definierten Puffer, um den Dateinamen zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, wenn erfolgreich oder andernfalls 1.

## <a name="remarks"></a>Bemerkungen

Wenn die mit NULL endenden Zeichenfolge, die den Dateinamen enthält, länger ist als der Puffer, wird der Dateiname von mciwnd abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetfilename**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





