---
title: MCIWNDM_NEW Meldung (VFW. h)
description: Mit der neuen mciwndm- \_ Meldung wird eine neue Datei für das aktuelle MCI-Gerät erstellt. Sie können diese Nachricht explizit oder mithilfe des mciwndnew-Makros senden.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741161"
---
# <a name="mciwndm_new-message"></a>Neue mciwndm- \_ Nachricht

Mit der **\_ neuen mciwndm** -Meldung wird eine neue Datei für das aktuelle MCI-Gerät erstellt. Sie können diese Nachricht explizit oder mithilfe des [**mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) -Makros senden.


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Zeiger auf einen Puffer, der den Namen des MCI-Geräts enthält, von dem die Datei verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





