---
title: WM_CAP_DLG_VIDEOCOMPRESSION (Vfw.h)
description: In der MELDUNG \_ WM CAP \_ DLG VIDEOCOMPRESSION wird ein Dialogfeld angezeigt, in dem der Benutzer eine Während des Erfassungsprozesses zu \_ verwendende Gruppe auswählen kann.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816aeb26455ba375b4446edc275ec4fbaa318b67b1fea64bd6049760f45d8235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135443"
---
# <a name="wm_cap_dlg_videocompression-message"></a>WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION-Meldung

In **der MELDUNG WM CAP \_ \_ DLG \_ VIDEOCOMPRESSION** wird ein Dialogfeld angezeigt, in dem der Benutzer während des Erfassungsprozesses einen Kasten auswählen kann, der verwendet werden soll. Die Liste der verfügbaren Produkte kann je nach video-Format variieren, das im Dialogfeld Videoformat des Erfassungstreibers ausgewählt ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) senden.


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Nachricht mit Erfassungstreibern, die Frames nur im \_ BI-RGB-Format bereitstellen. Diese Meldung ist besonders nützlich beim Schritterfassungsvorgang, um Erfassung und Komprimierung in einem einzelnen Vorgang zu kombinieren. Das Komprimieren von Frames mit einer Software, die im Rahmen eines Echtzeiterfassungs-Vorgangs verwendet wird, ist höchstwahrscheinlich zu zeitaufwändig.

Die Komprimierung wirkt sich nicht auf die Frames aus, die in die Zwischenablage kopiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





