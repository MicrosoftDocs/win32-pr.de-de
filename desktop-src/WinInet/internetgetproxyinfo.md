---
title: InternetGetProxyInfo-Funktion
description: Ruft Proxydaten für den Zugriff auf angegebene Ressourcen ab.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- InternetGetProxyInfo-Funktion WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76965f63afb751e810daa6feffe76774f03daaaf7278996b4c6800f0efa42dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113684"
---
# <a name="internetgetproxyinfo-function"></a>InternetGetProxyInfo-Funktion

> [!NOTE]
> Diese Funktion ist als veraltet markiert. Verwenden Sie für die Unterstützung des automatischen Proxys stattdessen DIE VERSION 5.1 der HTTP-Dienste (WinHTTP). Weitere Informationen finden Sie unter [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).

Ruft Proxydaten für den Zugriff auf angegebene Ressourcen ab. Diese Funktion kann nur durch dynamisches Verknüpfen mit "JSProxy.dll" aufgerufen werden.

## <a name="syntax"></a>Syntax

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszUrl* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die URL der HTTP-Zielressource angibt.

</dd> <dt>

*dwUrlLength* \[ In\]
</dt> <dd>

Die Größe der URL in Bytes, auf die *lpszUrl zeigt.*

</dd> <dt>

*lpszUrlHostName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Hostnamen der Ziel-URL angibt.

</dd> <dt>

*dwUrlHostNameLength* \[ In\]
</dt> <dd>

Die Größe des Hostnamens in Bytes, auf den *lpszUrlHostName zeigt.*

</dd> <dt>

*lplpszProxyHostName* \[ out\]
</dt> <dd>

Ein Zeiger auf die Adresse eines Puffers, der die URL des Proxys empfängt, der in einer HTTP-Anforderung für die angegebene Ressource verwendet werden soll. Die Anwendung ist für das Freigibt dieser Zeichenfolge verantwortlich.

</dd> <dt>

*lpdwProxyHostNameLength* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im *Puffer lplpszProxyHostName* zurückgegebenen Zeichenfolge in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.** Rufen Sie GetLastError auf, um erweiterte [**Fehlerdaten zu erhalten.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Zum Aufrufen **von InternetGetProxyInfo** müssen Sie mithilfe des definierten Funktionszeigertyps **pfnInternetGetProxyInfo** dynamisch eine Verknüpfung damit herstellen. Der folgende Codeausschnitt zeigt, wie Sie eine Instanz dieses Funktionszeigertyps deklarieren und anschließend initialisieren und aufrufen.

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

Wie alle anderen Aspekte der WinINet-API kann diese Funktion nicht sicher aus DllMain oder den Konstruktoren und Destruktoren globaler Objekte aufgerufen werden.

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
