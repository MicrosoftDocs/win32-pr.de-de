---
description: Bereinigt den Zustand für die Sitzung, die geöffnet wird, oder die aktuell geöffnete Sitzung.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: WF-displaysink CloseSession-Funktion (wsdsink. h)
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
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528160"
---
# <a name="wfddisplaysinkclosesession-function"></a>WF-displaysink CloseSession-Funktion

Bereinigt den Zustand für die Sitzung, die geöffnet wird, oder die aktuell geöffnete Sitzung.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsessionhandle* \[ in\]
</dt> <dd>

Das Handle, das über den letzten WFD-Aufruf empfangen wurde, zeigt den Rückruf Aufruf für [**\_ \_ \_ senkenbenachrichtigungen \_**](wfd-display-sink-notification-callback.md) an, der einen enthält

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

## <a name="remarks"></a>Bemerkungen

Ihre APP kann diese Funktion zum Beenden der miracast-Sitzung aus irgendeinem Grund aufruft. Ihre APP muss nicht aufgerufen werden, wenn Sie den **disconnectednotification** -Typ im Rückruf empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wifdisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs \_ Rückruf**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




