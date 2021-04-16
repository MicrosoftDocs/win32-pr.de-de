---
title: WM_CAP_SET_CALLBACK_ERROR Meldung (VFW. h)
description: Die WM- \_ Cap- \_ \_ Rückruf \_ Fehlermeldung legt eine Fehler Rückruffunktion in der Client Anwendung fest. Avicap ruft dieses Verfahren auf, wenn Fehler auftreten. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonerror-Makros senden.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477247"
---
# <a name="wm_cap_set_callback_error-message"></a>\_ \_ \_ Rückruf \_ Fehlermeldung für WM-Cap-Satz

Die **WM- \_ Cap- \_ \_ Rückruf \_ Fehlermeldung** legt eine Fehler Rückruffunktion in der Client Anwendung fest. Avicap ruft dieses Verfahren auf, wenn Fehler auftreten. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonerror**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Zeiger auf die Fehler Rückruffunktion vom Typ " [**caperrorcallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)". Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Fehler Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Anwendungen können optional eine Fehler Rückruffunktion festlegen. Wenn diese Einstellung festgelegt ist, wird die Fehler Prozedur von avicap in den folgenden Situationen aufgerufen:

-   Der Datenträger ist voll.
-   Ein Aufzeichnungs Fenster kann nicht mit einem Aufzeichnungs Treiber verbunden werden.
-   Ein Waveform-Audiogerät kann nicht geöffnet werden.
-   Die Anzahl der während der Erfassung verworfenen Frames überschreitet den angegebenen Prozentsatz.
-   Die Rahmen können aufgrund vertikaler Synchronisierungs Probleme nicht erfasst werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





