---
title: ICM_GETINFO Meldung (VFW. h)
description: Die ICM \_ GetInfo-Nachricht fragt einen Video Komprimierungs Treiber ab, um eine Beschreibung von sich selbst in einer icinfo-Struktur zurückzugeben.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO-Nachricht (Multimedia)
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
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337935"
---
# <a name="icm_getinfo-message"></a>ICM \_ GetInfo-Nachricht

Die **ICM \_ GetInfo** -Nachricht fragt einen Video Komprimierungs Treiber ab, um eine Beschreibung von sich selbst in einer [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) -Struktur zurückzugeben.


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Zeiger auf eine **icinfo** -Struktur, die Informationen enthalten soll.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von **icinfo**(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe von [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) (in Bytes) oder 0 (null) zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Bemerkungen

Normalerweise senden Anwendungen diese Nachricht, um eine Liste der installierten Kompressoren anzuzeigen.

Der Treiber sollte alle Elemente der [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) -Struktur mit Ausnahme von **szdriver** ausfüllen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





