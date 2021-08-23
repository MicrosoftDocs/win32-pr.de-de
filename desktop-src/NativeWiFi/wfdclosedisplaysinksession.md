---
description: Bereinigt den Zustand für die Sitzung, die geöffnet wird, oder die derzeit geöffnete Sitzung.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: WFDDisplaySinkCloseSession-Funktion (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7e8169c541535eb2c5adfd0959da47cee4951750687f7d926798534ddc7cbf88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064900"
---
# <a name="wfddisplaysinkclosesession-function"></a>WFDDisplaySinkCloseSession-Funktion

Bereinigt den Zustand für die Sitzung, die geöffnet wird, oder die derzeit geöffnete Sitzung.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSessionHandle* \[ In\]
</dt> <dd>

Das Handle, das über den letzten [**WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK-Aufruf**](wfd-display-sink-notification-callback.md) empfangen wurde, der einen enthalten hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

## <a name="remarks"></a>Hinweise

Ihre App kann diese Funktion aufrufen, um die Miracast Sitzung aus beliebigem Grund zu beenden. Ihre App muss sie nicht aufrufen, wenn sie den **DisconnectedNotification-Typ** in ihrem Rückruf empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_ \_ WFD-ANZEIGESENKENBENACHRICHTIGUNGSRÜCKRUF \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




