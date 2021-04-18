---
title: Rasadminportdisconnect-Funktion (rassapi. h)
description: Die rasadminportdisconnect-Funktion trennt einen Port, der zurzeit verwendet wird.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- Rasadminportdisconnect-Funktion (RAS)
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
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361384"
---
# <a name="rasadminportdisconnect-function"></a>Rasadminportdisconnect-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminportdisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) -Funktion verwenden.\]

Die **rasadminportdisconnect** -Funktion trennt einen Port, der zurzeit verwendet wird.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Windows NT/Windows 2000-RAS-Servers angibt. Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.

</dd> <dt>

*lpszport* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Wert                                                                                               | Bedeutung                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Port.**</dt> </dl> | Der angegebene Port ist ungültig.<br/>    |
| <dl> <dt>**NERR \_ usernotfound**</dt> </dl>   | Der Port wird derzeit nicht verwendet.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsfunktionen](ras-server-administration-functions.md)
</dt> </dl>

 

