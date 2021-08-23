---
title: ICM_DRAW (Vfw.h)
description: Die ICM DRAW-Nachricht benachrichtigt einen Renderingtreiber, einen Datenrahmen zu dekomprimieren und \_ auf den Bildschirm zu zeichnen.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW von Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44216e523da62e0dde22abed8d88b9b8aacd8f68119a88f3177f45ecd910029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784990"
---
# <a name="icm_draw-message"></a>\_ICM DRAW-Nachricht

Die **ICM \_ DRAW-Nachricht** benachrichtigt einen Renderingtreiber, um einen Datenrahmen zu dekomprimieren und auf den Bildschirm zu zeichnen.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Zeiger auf eine [**ICDRAW-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-icdraw)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe von [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich oder andernfalls ein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Wenn das ICDRAW UPDATE-Flag im \_ **dwFlags-Member** von [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)festgelegt ist, ist der zum Zeichnen verwendete Bildschirmbereich ungültig und muss aktualisiert werden. Der Umfang der Aktualisierung hängt vom Inhalt des **lpData-Mitglieds** ab.

Wenn **lpData** **NULL ist,** sollte der Treiber das gesamte Zielrechteck mit dem aktuellen Bild aktualisieren. Wenn der Treiber eine Kopie des Bilds in einem Off-Screen-Puffer verwaltet, kann diese Meldung fehlschlagen. Wenn **lpData** nicht **NULL ist,** sollte der Treiber die Daten zeichnen und sicherstellen, dass das gesamte Ziel aktualisiert wird.

Wenn das \_ ICDRAW-FLAG BZW. DAS ICDRAW-FLAG in **dwFlags** festgelegt ist, möchte die aufrufende Anwendung, dass der Treiber so schnell wie möglich fortgesetzt wird, möglicherweise wird der Bildschirm nicht einmal aktualisiert.

Wenn das ICDRAW \_ PREROLL-Flag in **dwFlags** festgelegt ist, handelt es sich bei diesem Videoframe um vorläufige Informationen und sollte nach Möglichkeit nicht angezeigt werden. Wenn die Wiedergabe beispielsweise ab Frame 10 beginnen soll und Frame 0 der nächste vorherige Keyframe ist, wird für Frames von 0 bis 9 ICDRAW \_ PREROLL festgelegt.

Wenn der Treiber Daten in einen Puffer dekomprimieren soll, senden Sie die ICM [**\_ DECOMPRESS-Nachricht.**](icm-decompress.md)

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

 

 





