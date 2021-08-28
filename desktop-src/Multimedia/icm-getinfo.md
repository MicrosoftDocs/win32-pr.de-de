---
title: ICM_GETINFO (Vfw.h)
description: Die ICM GETINFO-Nachricht fragt einen Videokomprimierungstreiber ab, um eine Beschreibung von \_ sich selbst in einer ICINFO-Struktur zurück zu geben.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173f510642b807a0e4c4a8c5c84d6d4de2aa7ce55cc0707eccabf5421cf98a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690810"
---
# <a name="icm_getinfo-message"></a>\_ICM GETINFO-Nachricht

Die **ICM \_ GETINFO-Nachricht** fragt einen Videokomprimierungstreiber ab, um eine Beschreibung von sich selbst in einer [**ICINFO-Struktur zurück**](/windows/desktop/api/Vfw/ns-vfw-icinfo) zu geben.


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Zeiger auf eine **ICINFO-Struktur,** die Informationen enthalten soll.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe von **ICINFO** in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe von [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) in Bytes oder 0 (null) zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

In der Regel senden Anwendungen diese Meldung, um eine Liste der installierten 2007-Computer anzuzeigen.

Der Treiber sollte alle Member der [**ICINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-icinfo) mit Ausnahme **von szDriver ausfüllen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





