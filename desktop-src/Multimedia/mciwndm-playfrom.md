---
title: MCIWNDM_PLAYFROM Meldung (VFW. h)
description: Die mciwndm \_ playfrom-Meldung gibt den Inhalt eines MCI-Geräts vom angegebenen Speicherort bis zum Ende des Inhalts oder bis zur Beendigung der Wiedergabe durch einen anderen Befehl wieder. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndplayfrom senden.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949530"
---
# <a name="mciwndm_playfrom-message"></a>Mciwndm \_ playfrom-Meldung

Die **mciwndm \_ playfrom** -Meldung gibt den Inhalt eines MCI-Geräts vom angegebenen Speicherort bis zum Ende des Inhalts oder bis zur Beendigung der Wiedergabe durch einen anderen Befehl wieder. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) senden.


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*
</dt> <dd>

Start Speicherort. Die Einheiten für den Start Speicherort hängen vom aktuellen Zeitformat ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Sie können auch einen Start-und einen endspeicherort für die Wiedergabe angeben, indem Sie das [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) -Makro verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[**Mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





