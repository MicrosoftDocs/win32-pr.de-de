---
title: WM_CAP_DRIVER_GET_VERSION Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ Driver \_ get \_ Version" gibt die Versionsinformationen des Aufzeichnungs Treibers zurück, der mit einem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des capdrivergetversion-Makros senden.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345923"
---
# <a name="wm_cap_driver_get_version-message"></a>WM- \_ Cap- \_ Treiber Version der \_ \_ Nachricht erhalten

Die Meldung " **WM \_ Cap \_ Driver \_ get \_ Version** " gibt die Versionsinformationen des Aufzeichnungs Treibers zurück, der mit einem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des [**capdrivergetversion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) -Makros senden.


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) des Anwendungs definierten Puffers, auf den von **szver** verwiesen wird.

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szver*
</dt> <dd>

Ein Zeiger auf einen Anwendungs definierten Puffer, der verwendet wird, um die Versionsinformationen als NULL-terminierte Zeichenfolge zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.

## <a name="remarks"></a>Bemerkungen

Die Versionsinformationen sind eine Text Zeichenfolge, die aus dem Ressourcenbereich des Treibers abgerufen wird. Anwendungen sollten für diese Zeichenfolge ungefähr 40 Byte zuordnen. Wenn keine Versionsinformationen verfügbar sind, wird eine **null** -Zeichenfolge zurückgegeben.

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

 

 





