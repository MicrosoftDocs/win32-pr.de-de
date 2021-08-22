---
title: MCIWNDM_OPEN (Vfw.h)
description: Die MCIWNDM \_ OPEN-Meldung öffnet ein MCI-Gerät und ordnet es einem MCIWnd-Fenster zu.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN-Nachricht Windows Multimedia
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
ms.openlocfilehash: 03bebf9573303e3560b385425e7642106120c41456a21c1c4b80bc158328a864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428900"
---
# <a name="mciwndm_open-message"></a>MCIWNDM \_ OPEN-Nachricht

Die **MCIWNDM \_ OPEN-Meldung** öffnet ein MCI-Gerät und ordnet es einem MCIWnd-Fenster zu. Für MCI-Geräte, die Datendateien verwenden, kann dieses Makro auch eine angegebene Datendatei öffnen, eine neue zu erstellende Datei benennen oder ein Dialogfeld anzeigen, in dem der Benutzer eine zu öffnende Datei auswählen kann. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndOpen-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) senden.


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Flags, die dem zu öffnenden Gerät oder der zu öffnenden Datei zugeordnet sind. Das Flag MCIWNDOPENF NEW gibt an, dass eine neue Datei mit dem \_ in **szFile angegebenen Namen erstellt werden soll.**

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den datei- oder MCI-Gerätenamen identifiziert, der geöffnet werden soll. Geben Sie 1 für diesen Parameter an, um das Dialogfeld Öffnen anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





