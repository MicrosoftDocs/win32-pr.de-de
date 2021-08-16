---
title: MCIWNDM_GETMODE (Vfw.h)
description: Die MCIWNDM \_ GETMODE-Nachricht ruft den aktuellen Betriebsmodus eines MCI-Geräts ab. MCI-Geräte verfügen über mehrere Betriebsmodi, die durch Konstanten festgelegt werden. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetMode-Makros senden.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE von Windows Multimedia
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
ms.openlocfilehash: 645d7a660df8d22cb2adb70a775d5431eb31dc986b502bb4dbb36b1963ce06f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429270"
---
# <a name="mciwndm_getmode-message"></a>MCIWNDM \_ GETMODE-Nachricht

Die **MCIWNDM \_ GETMODE-Nachricht** ruft den aktuellen Betriebsmodus eines MCI-Geräts ab. MCI-Geräte verfügen über mehrere Betriebsmodi, die durch Konstanten festgelegt werden. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetMode-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) senden.


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Größe des Puffers in Bytes.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Zeiger auf den anwendungsdefinierten Puffer, der zum Zurückgeben des Modus verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die der MCI-Konstante entspricht, die den Modus definiert.

## <a name="remarks"></a>Hinweise

Wenn die mit NULL beendete Zeichenfolge, die den Modus beschreibt, länger als der Puffer ist, wird sie abgeschnitten.

Nicht alle Geräte können in jedem Modus ausgeführt werden. Das MCIAVI-Gerät ist beispielsweise ein Wiedergabegerät. Der Aufzeichnungsmodus wird nicht unterstützt. Die folgenden Modi können mithilfe von **MCIWNDM \_ GETMODE abgerufen werden.**



| Betriebsmodus | MCI-Konstante          |
|----------------|-----------------------|
| nicht bereit      | MCI-MODUS \_ \_ NICHT \_ BEREIT |
| öffnen           | \_MCI-MODUS \_ GEÖFFNET       |
| angehalten         | PAUSE IM \_ \_ MCI-MODUS      |
| Wiedergabe        | WIEDERGABE IM \_ \_ MCI-MODUS       |
| Aufzeichnung      | \_ \_ MCI-MODUSDATENSATZ     |
| Suchen        | MCI \_ MODE \_ SEEK       |
| stopped        | BEENDEN DES \_ \_ MCI-MODUS       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





