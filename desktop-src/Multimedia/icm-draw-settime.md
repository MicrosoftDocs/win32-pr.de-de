---
title: ICM_DRAW_SETTIME Meldung (VFW. h)
description: Der ICM \_ Draw \_ setTime stellt Synchronisierungs Informationen für einen renderingtreiber bereit, der die zeitliche Steuerung von Zeichnungs Frames behandelt.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858810"
---
# <a name="icm_draw_settime-message"></a>ICM \_ Draw- \_ setTime-Meldung

Der **ICM \_ Draw \_ setTime** stellt Synchronisierungs Informationen für einen renderingtreiber bereit, der die zeitliche Steuerung von Zeichnungs Frames behandelt. Die Synchronisierungs Informationen sind die Beispiel Nummer des Frames, der gezeichnet werden soll. Sie können diese Nachricht explizit oder mithilfe des [**icdrawsettime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) -Makros senden.


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lptime*
</dt> <dd>

Die Stichproben Nummer des zu Rendering enden Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Normalerweise vergleicht der Treiber den angegebenen Wert mit der dem Zeitpunkt der internen Uhr zugeordneten Frame Nummer und versucht, die beiden zu synchronisieren, wenn der Unterschied signifikant ist.

Verwenden Sie diese Meldung, wenn die Hardware eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt und die Hardware auf einem externen Synchronisierungs Signal basiert (die Hardware wird nicht als Synchronisierungs Master verwendet).

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

 

 





