---
title: RasAdminServerGetInfo-Funktion (Rassapi.h)
description: Die RasAdminServerGetInfo-Funktion ruft die Serverkonfiguration eines RAS-Servers ab.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo-Funktion RAS
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
ms.openlocfilehash: 1f6f83f7310700e774692d876bda979343da80aa45ea8012bf187e50f0af67bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028450"
---
# <a name="rasadminservergetinfo-function"></a>RasAdminServerGetInfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminServerGetInfo-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) verwenden.\]

Die **RasAdminServerGetInfo-Funktion** ruft die Serverkonfiguration eines RAS-Servers ab.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Zeiger auf eine mit **NULL beendete** Unicode-Zeichenfolge, die den Namen des Windows NT/Windows 2000 RAS-Servers angibt. Wenn dieser Parameter **NULL ist,** gibt die Funktion Informationen zum lokalen Computer zurück. Geben Sie den Namen mit den \\ \\ führenden Zeichen " " im folgenden Formular an: \\ \\ *Servername*.

</dd> <dt>

*pRasServer0* \[ out\]
</dt> <dd>

Zeiger auf die [**RAS \_ SERVER \_ 0-Struktur,**](ras-server-0-str.md) die die Anzahl der auf dem Server konfigurierten Ports, die Anzahl aktuell verwendeter Ports und die Serverversionsnummer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode. Mögliche Fehlercodes sind diejenigen, die von [**GetLastError für**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) die [**CallNamedPipe-Funktion zurückgegeben**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) werden. Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie **getLastError nicht auf.**

## <a name="remarks"></a>Hinweise

Um alle RAS-Server in einer Domäne aufzählen zu können, rufen Sie die [**NetServerEnum-Funktion**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) auf, und geben Sie SV TYPE DIALIN für \_ den \_ *Servertype-Parameter* an.

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
</dt> <dt>

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**RAS \_ SERVER \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

