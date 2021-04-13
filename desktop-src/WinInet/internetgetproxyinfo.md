---
title: InternetGetProxyInfo-Funktion
description: Ruft Proxy Daten für den Zugriff auf angegebene Ressourcen ab.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Internetgetproxyinfo-Funktion WinInet
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
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391927"
---
# <a name="internetgetproxyinfo-function"></a>InternetGetProxyInfo-Funktion

> [!NOTE]
> Diese Funktion ist als veraltet markiert. Verwenden Sie für die aktivierter automatischer Proxy-Unterstützung stattdessen HTTP-Dienste (WinHTTP), Version 5,1. Weitere Informationen finden Sie [unter WinHTTP AutoProxy-Unterstützung](../winhttp/winhttp-autoproxy-support.md).

Ruft Proxy Daten für den Zugriff auf angegebene Ressourcen ab. Diese Funktion kann nur durch dynamisches Verknüpfen mit "JSProxy.dll" aufgerufen werden.

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

*lpszurl* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die URL der http-Ziel Ressource angibt.

</dd> <dt>

*dwurllength* \[ in\]
</dt> <dd>

Die Größe (in Bytes) der URL, auf die *lpszurl* zeigt.

</dd> <dt>

*lpszurlhostname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Hostnamen der Ziel-URL angibt.

</dd> <dt>

*dwurlhostnamelength* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Host namens, auf den von *lpszurlhostname* verwiesen wird.

</dd> <dt>

*lplpszproxyhostname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Adresse eines Puffers, der die URL des Proxys empfängt, der in einer HTTP-Anforderung für die angegebene Ressource verwendet werden soll. Die Anwendung ist dafür verantwortlich, diese Zeichenfolge freizugeben.

</dd> <dt>

*lpdwproxyhostnamelength* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Zeichenfolge in Bytes empfängt, die im *lplpszproxyhostname* -Puffer zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . Um erweiterte Fehler Daten abzurufen, nennen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Bemerkungen

Um **internetgetproxyinfo** aufzurufen, müssen Sie dynamisch mit dem definierten Funktions Zeigertyp **pfninternetgetproxyinfo** mit ihm verknüpfen. Der folgende Code Ausschnitt zeigt, wie Sie eine Instanz dieses Funktionszeiger Typs deklarieren und anschließend initialisieren und aufzurufen.

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

Wie alle anderen Aspekte der WinInet-API kann diese Funktion nicht sicher innerhalb von DllMain oder den Konstruktoren und Dekonstruktoren von globalen Objekten aufgerufen werden.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[**Internetinitializeautoproxydll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**Internetdeinitializeautoproxydll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**Detectautoproxyurl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
