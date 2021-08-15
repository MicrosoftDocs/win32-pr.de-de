---
title: WM_CAP_DRIVER_GET_VERSION (Vfw.h)
description: Die Meldung WM CAP DRIVER GET VERSION gibt die Versionsinformationen des Erfassungstreibers zurück, der \_ \_ mit einem \_ \_ Erfassungsfenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des Makros capDriverGetVersion senden.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION-Nachricht Windows Multimedia
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
ms.openlocfilehash: 49f6bed4513383c5dd889639a78e9f00e409fe347bfd6b64b112ea830571ae55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687090"
---
# <a name="wm_cap_driver_get_version-message"></a>WM CAP DRIVER GET VERSION message (WM \_ CAP \_ DRIVER GET \_ \_ VERSION-Meldung)

Die **Meldung WM CAP DRIVER GET VERSION \_ \_ \_ \_ gibt** die Versionsinformationen des Erfassungstreibers zurück, der mit einem Erfassungsfenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) senden.


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe des anwendungsdefinierten Puffers in Bytes, auf den **szVer verweist.**

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

Zeiger auf einen anwendungsdefinierten Puffer, der verwendet wird, um die Versionsinformationen als auf NULL beendete Zeichenfolge zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, oder **FALSE,** wenn das Erfassungsfenster nicht mit einem Erfassungstreiber verbunden ist.

## <a name="remarks"></a>Hinweise

Die Versionsinformationen sind eine Textzeichenfolge, die aus dem Ressourcenbereich des Treibers abgerufen wird. Anwendungen sollten für diese Zeichenfolge ungefähr 40 Bytes zuordnen. Wenn keine Versionsinformationen verfügbar sind, wird eine **NULL-Zeichenfolge** zurückgegeben.

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

 

 





