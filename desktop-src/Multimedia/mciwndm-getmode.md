---
title: MCIWNDM_GETMODE Meldung (VFW. h)
description: Die mciwndm \_ getMode-Nachricht Ruft den aktuellen Betriebsmodus eines MCI-Geräts ab. MCI-Geräte verfügen über mehrere Betriebsmodi, die durch Konstanten festgelegt werden. Sie können diese Nachricht explizit oder mithilfe des mciwndgetmode-Makros senden.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102842"
---
# <a name="mciwndm_getmode-message"></a>Mciwndm \_ getMode-Meldung

Die **mciwndm \_ getMode** -Nachricht Ruft den aktuellen Betriebsmodus eines MCI-Geräts ab. MCI-Geräte verfügen über mehrere Betriebsmodi, die durch Konstanten festgelegt werden. Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetmode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) -Makros senden.


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Nest*
</dt> <dd>

Größe (in Bytes) des Puffers.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ein Zeiger auf den Anwendungs definierten Puffer, der verwendet wird, um den Modus zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der MCI-Konstante entspricht, die den Modus definiert.

## <a name="remarks"></a>Bemerkungen

Wenn die auf NULL endenden Zeichenfolge, die den Modus beschreibt, länger als der Puffer ist, wird Sie abgeschnitten.

Nicht alle Geräte können in jedem Modus betrieben werden. Beispielsweise ist das MCIAVI-Gerät ein Wiedergabe Gerät. der Aufzeichnungsmodus wird nicht unterstützt. Die folgenden Modi können mithilfe von **mciwndm \_ getMode** abgerufen werden.



| Betriebsmodus | MCI-Konstante          |
|----------------|-----------------------|
| nicht bereit      | MCI- \_ Modus \_ nicht \_ bereit |
| open           | MCI- \_ Modus \_ geöffnet       |
| angehalten         | MCI- \_ Modus anhalten \_      |
| Wiedergabe        | MCI- \_ Modus \_ abspielen       |
| Aufzeichnung      | MCI- \_ Modus- \_ Datensatz     |
| Suchen        | MCI- \_ Modus- \_ Suche       |
| stopped        | MCI- \_ Modus wird \_ beendet       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetmode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





