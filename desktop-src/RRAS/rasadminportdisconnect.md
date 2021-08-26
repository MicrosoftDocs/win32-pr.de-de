---
title: RasAdminPortDisconnect-Funktion (Rassapi.h)
description: Die RasAdminPortDisconnect-Funktion trennt die Verbindung mit einem port, der derzeit verwendet wird.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect-Funktion RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a0f3abf4cee54f92c9bfd846557623de5e23fffd4724a701ca7c04aa818af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028520"
---
# <a name="rasadminportdisconnect-function"></a>RasAdminPortDisconnect-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminPortDisconnect-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) verwenden.\]

Die **RasAdminPortDisconnect-Funktion** trennt die Verbindung mit einem port, der derzeit verwendet wird.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des nt Windows/Windows 2000-RAS-Servers angibt. Geben Sie den Namen mit den \\ \\ führenden Zeichen " " im folgenden Formular an: \\ \\ *Servername*.

</dd> <dt>

*lpszPort* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Wert                                                                                               | Bedeutung                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**FEHLER: \_ \_ UNGÜLTIGER PORT**</dt> </dl> | Der angegebene Port ist ungültig.<br/>    |
| <dl> <dt>**NERR \_ UserNotFound**</dt> </dl>   | Der Port wird derzeit nicht verwendet.<br/> |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsfunktionen](ras-server-administration-functions.md)
</dt> </dl>

 

