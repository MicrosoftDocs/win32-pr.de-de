---
title: MCIWNDM_GETDEVICE Meldung (VFW. h)
description: Die mciwndm \_ getdevice-Nachricht Ruft den Namen des aktuell geöffneten MCI-Geräts ab. Sie können diese Nachricht explizit oder mit dem mciwndgetdevice-Makro senden.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475534"
---
# <a name="mciwndm_getdevice-message"></a>Mciwndm \_ getdevice-Meldung

Die **mciwndm \_ getdevice** -Nachricht Ruft den Namen des aktuell geöffneten MCI-Geräts ab. Sie können diese Nachricht explizit oder mit dem [**mciwndgetdevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) -Makro senden.


```C++
MCIWNDM_GETDEVICE 
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

Zeiger auf einen Anwendungs definierten Puffer, um den Gerätenamen zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, wenn erfolgreich, andernfalls ein Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn die mit NULL endenden Zeichenfolge, die den Gerätenamen enthält, länger ist als der Puffer, wird Sie von mciwnd abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





