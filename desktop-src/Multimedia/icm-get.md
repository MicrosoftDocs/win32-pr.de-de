---
title: ICM_GET Meldung (VFW. h)
description: Die ICM \_ GET-Nachricht Ruft einen von der Anwendung definierten DWORD-Wert von einem Video Komprimierungs Treiber ab.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740496"
---
# <a name="icm_get-message"></a>ICM- \_ GET-Nachricht

Die **ICM \_ Get** -Nachricht Ruft einen von der Anwendung definierten **DWORD** -Wert von einem Video Komprimierungs Treiber ab.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*teuren*
</dt> <dd>

Ein Zeiger auf einen Speicherblock, der mit dem aktuellen Zustand aufgefüllt werden soll. Sie können auch **null** angeben, um den von den Zustandsinformationen benötigten Arbeitsspeicher zu ermitteln.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*betrieben*
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe des Arbeitsspeichers in Bytes zurück, der zum Speichern der Statusinformationen erforderlich ist.

## <a name="remarks"></a>Bemerkungen

Die Struktur, die zum Darstellen von Zustandsinformationen verwendet wird, ist Treiber spezifisch und wird vom Treiber definiert.

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

 

 





