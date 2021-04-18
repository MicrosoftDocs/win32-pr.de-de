---
title: WM_CAP_DRIVER_GET_NAME Meldung (VFW. h)
description: Die Meldung "WM- \_ Cap- \_ Treiber \_ get \_ Name" gibt den Namen des Aufzeichnungs Treibers zurück, der mit dem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des capdrivergetname-Makros senden.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475858"
---
# <a name="wm_cap_driver_get_name-message"></a>WM- \_ Cap- \_ Treiber get- \_ \_ namens Meldung

Die Meldung " **WM- \_ Cap- \_ Treiber \_ get \_ Name** " gibt den Namen des Aufzeichnungs Treibers zurück, der mit dem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des [**capdrivergetname**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) -Makros senden.


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) des Puffers, auf den von **szName** verwiesen wird.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ein Zeiger auf einen Anwendungs definierten Puffer, der verwendet wird, um den Gerätenamen als eine auf NULL endende Zeichenfolge zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.

## <a name="remarks"></a>Bemerkungen

Der Name ist eine Text Zeichenfolge, die aus dem Ressourcenbereich des Treibers abgerufen wird. Anwendungen sollten für diese Zeichenfolge ungefähr 80 Byte zuordnen. Wenn der Treiber keine namens Ressource enthält, wird der vollständige Pfadname des Treibers, der in der Registrierung oder in der SYSTEM.INI Datei aufgeführt ist, zurückgegeben.

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

 

 





