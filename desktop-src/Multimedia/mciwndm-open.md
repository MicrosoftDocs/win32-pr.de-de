---
title: MCIWNDM_OPEN Meldung (VFW. h)
description: Die Meldung mciwndm \_ Open öffnet ein MCI-Gerät und ordnet es einem mciwnd-Fenster zu.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103435"
---
# <a name="mciwndm_open-message"></a>Meldung zum Öffnen von mciwndm \_

Die Meldung **mciwndm \_ Open** öffnet ein MCI-Gerät und ordnet es einem mciwnd-Fenster zu. Bei MCI-Geräten, die Datendateien verwenden, kann dieses Makro auch eine bestimmte Datendatei öffnen, eine neue zu erstellende Datei benennen oder ein Dialogfeld anzeigen, in dem der Benutzer eine Datei auswählen kann, die geöffnet werden soll. Sie können diese Nachricht explizit oder mithilfe des [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) -Makros senden.


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Flags, die dem zu öffnenden Gerät oder der Datei zugeordnet sind. Das neue mciwndopenf- \_ Flag gibt an, dass eine neue Datei mit dem Namen erstellt werden soll, der in **szFile** angegeben ist.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den zu öffnenden Dateinamen oder MCI-Gerätenamen identifiziert. Geben Sie 1 für diesen Parameter an, um das Dialogfeld Öffnen anzuzeigen.

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

[**Mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





