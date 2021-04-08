---
title: MCIWNDM_SETTIMERS Meldung (VFW. h)
description: Die mciwndm \_ settimers-Nachricht legt die Aktualisierungs Zeiträume fest, die von mciwnd verwendet werden, um die TrackBar im mciwnd-Fenster zu aktualisieren, die in der Fenstertitelleiste angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740233"
---
# <a name="mciwndm_settimers-message"></a>Mciwndm \_ settimers-Nachricht

Die **mciwndm \_ settimers** -Nachricht legt die Aktualisierungs Zeiträume fest, die von mciwnd verwendet werden, um die TrackBar im mciwnd-Fenster zu aktualisieren, die in der Fenstertitelleiste angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndsettimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) senden.


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*enden*
</dt> <dd>

Aktualisierungs Zeitraum, der von mciwnd verwendet wird, wenn es sich um das aktive Fenster handelt. Der Standardwert ist 500 Millisekunden. Der Speicher für diesen Wert ist auf 16 Bits beschränkt.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*VSTE*
</dt> <dd>

Update Zeitraum, der von mciwnd verwendet wird, wenn es sich um das inaktive Fenster handelt. Der Standardwert beträgt 2.000 Millisekunden. Der Speicher für diesen Wert ist auf 16 Bits beschränkt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndsettimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





