---
title: ICM_GETSTATE Meldung (VFW. h)
description: Die ICM \_ GetState-Nachricht fragt einen Video Komprimierungs Treiber ab, um die aktuelle Konfiguration in einem Speicherblock zurückzugeben, oder um die Menge an Arbeitsspeicher zu ermitteln, die zum Abrufen der Konfigurationsinformationen erforderlich ist.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106550"
---
# <a name="icm_getstate-message"></a>ICM \_ GetState-Nachricht

Die **ICM \_ GetState** -Nachricht fragt einen Video Komprimierungs Treiber ab, um die aktuelle Konfiguration in einem Speicherblock zurückzugeben, oder um die Menge an Arbeitsspeicher zu ermitteln, die zum Abrufen der Konfigurationsinformationen erforderlich ist. Sie können diese Nachricht explizit oder mithilfe des [**icgetstate**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) -Makros senden.


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*teuren*
</dt> <dd>

Ein Zeiger auf einen Speicherblock, der die aktuellen Konfigurationsinformationen enthalten soll. Sie können **null** für diesen Parameter angeben, um den für die Konfigurationsinformationen erforderlichen Arbeitsspeicher zu bestimmen, wie in [**icgetstatus esize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*betrieben*
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn *PV* den Wert **null** hat, wird die Menge an Arbeitsspeicher in Bytes zurückgegeben, die für Konfigurationsinformationen erforderlich ist.

Wenn *PV* nicht **null** ist, wird bei erfolgreicher Ausführung von ICERR OK zurückgegeben, \_ andernfalls wird ein Fehler zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Struktur, die zum Darstellen von Konfigurationsinformationen verwendet wird, ist Treiber spezifisch und wird vom Treiber definiert.

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

 

 





