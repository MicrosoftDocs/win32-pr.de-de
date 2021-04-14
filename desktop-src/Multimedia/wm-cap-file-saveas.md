---
title: WM_CAP_FILE_SAVEAS Meldung (VFW. h)
description: Die "WM Cap"- \_ \_ Datei " \_ SaveAs" kopiert den Inhalt der Erfassungs Datei in eine andere Datei. Sie können diese Nachricht explizit oder mithilfe des "capfilesaveas"-Makros senden.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391712"
---
# <a name="wm_cap_file_saveas-message"></a>\_Datei " \_ \_ SaveAs" der WM-Cap-Datei

Die " **WM Cap"- \_ Datei " \_ \_ SaveAs** " kopiert den Inhalt der Erfassungs Datei in eine andere Datei. Sie können diese Nachricht explizit oder mithilfe des " [**capfilesaveas**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) "-Makros senden.


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die den Namen der zum Kopieren der Datei verwendeten Zieldatei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ändert nicht den Namen oder den Inhalt der aktuellen Erfassungs Datei.

Wenn der Kopiervorgang aufgrund eines vollständigen Festplattenfehlers nicht erfolgreich ist, wird die Zieldatei automatisch gelöscht.

In der Regel wird eine Erfassungs Datei für das größte erwartete Erfassungs Segment reserviert, und nur ein Teil davon kann zum Erfassen von Daten verwendet werden. Diese Nachricht kopiert nur den Teil der Datei, in der die Aufzeichnungsdaten enthalten sind.

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

 

 





