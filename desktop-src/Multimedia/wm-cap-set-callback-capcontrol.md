---
title: WM_CAP_SET_CALLBACK_CAPCONTROL Meldung (VFW. h)
description: Die \_ \_ \_ capcontrol-Rückruffunktion für die WM-Abdeckung \_ legt eine Rückruffunktion in der Anwendung fest, die ihr ein präzises Aufzeichnungs Steuerelement gibt. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackoncapcontrol-Makros senden.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338741"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>WM- \_ Cap-Rückruf-Rückruf- \_ \_ \_ capcontrol-Meldung

Die **\_ \_ \_ \_ capcontrol-Rückruf** Funktion für die WM-Abdeckung legt eine Rückruffunktion in der Anwendung fest, die ihr ein präzises Aufzeichnungs Steuerelement gibt. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackoncapcontrol**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Ein Zeiger auf die Rückruffunktion vom Typ [**capcontrolcallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback). Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Eine einzelne Rückruffunktion wird verwendet, um der Anwendung die genaue Kontrolle über die Momente zu verschaffen, in denen die streamingerfassung beginnt und abgeschlossen wird. Im Aufzeichnungs Fenster wird zuerst die Prozedur aufgerufen, bei der *nState* auf controlcallback \_ Preroll festgelegt wurde, nachdem alle Puffer zugeordnet wurden und alle anderen Aufzeichnungs Vorbereitungen abgeschlossen sind. Dadurch erhält die Anwendung die Möglichkeit, Videoquellen vorab zu überarbeiten und die Rückruffunktion zu dem Zeitpunkt zurückzugeben, zu dem die Aufzeichnung beginnt. Der Rückgabewert **true** von der Rückruffunktion setzt die Erfassung fort, und der Rückgabewert **false** bricht Capture ab. Nachdem die Erfassung begonnen hat, wird diese Rückruffunktion häufig aufgerufen, wobei *nState* auf controlcallback Capture festgelegt ist, \_ damit die Anwendung die Erfassung beenden kann, indem **false** zurückgegeben wird.

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

 

 





