---
title: Rasadminservergetinfo-Funktion (rassapi. h)
description: Die rasadminservergetinfo-Funktion Ruft die Serverkonfiguration eines RAS-Servers ab.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- Rasadminservergetinfo-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372637"
---
# <a name="rasadminservergetinfo-function"></a>Rasadminservergetinfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminservergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) -Funktion verwenden.\]

Die **rasadminservergetinfo** -Funktion Ruft die Serverkonfiguration eines RAS-Servers ab.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit **null** endenden Unicode-Zeichenfolge, die den Namen des Windows NT/Windows 2000-RAS-Servers angibt. Wenn dieser Parameter **null** ist, gibt die Funktion Informationen über den lokalen Computer zurück. Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.

</dd> <dt>

*pRasServer0* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**RAS- \_ Server- \_ 0**](ras-server-0-str.md) -Struktur, die die Anzahl der auf dem Server konfigurierten Ports, die Anzahl der derzeit verwendeten Ports und die Server Versionsnummer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode. Mögliche Fehlercodes sind diejenigen, die von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) für die [**callnamedpipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) -Funktion zurückgegeben werden. Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " **GetLastError**" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Um alle RAS-Server in einer Domäne aufzulisten, geben Sie die [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) -Funktion an, und geben Sie \_ \_ für den *Server Type* -Parameter den Befehl SV Type Dialin an.

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
</dt> <dt>

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**RAS- \_ Server \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

