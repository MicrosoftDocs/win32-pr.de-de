---
description: WinHTTP implementiert das WPAD-Protokoll mithilfe der WinHttpGetProxyForUrl-Funktion zusammen mit zwei unterstützenden Hilfsprogrammfunktionen, winhttpdetectautoproxyconfigurl und WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: WinHTTP AutoProxy-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd4cf8289add4c72c2266df4bb9025e0b4c1aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958939"
---
# <a name="winhttp-autoproxy-functions"></a>WinHTTP AutoProxy-Funktionen

WinHTTP implementiert das WPAD-Protokoll mithilfe der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion zusammen mit zwei unterstützenden Hilfsprogrammfunktionen, [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) und [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

Die AutoProxy-Unterstützung ist nicht vollständig in den HTTP-Stapel in WinHTTP integriert. Bevor eine Anforderung gesendet wird, muss die Anwendung [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) aufrufen, um den Namen eines Proxy Servers zu erhalten, und dann [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mithilfe des **WinHTTP- \_ options \_ Proxys** aufrufen, um die Proxykonfiguration für das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellte WinHTTP-Anforderungs Handle festzulegen.

Die [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion kann alle drei Schritte des WPAD-Protokolls ausführen, das in der vorherigen Übersicht beschrieben wurde: (1) ermitteln der PAC-URL, (2) laden Sie die PAC-Skriptdatei herunter, (3) führen Sie den Skriptcode aus, und geben Sie die Proxykonfiguration in einer **WinHTTP- \_ Proxy \_ Informations** Struktur zurück. Wenn die Anwendung im Voraus die PAC-URL kennt, kann Sie diese als " **WinHttpGetProxyForUrl**" angeben.

Im folgenden Beispielcode wird AutoProxy verwendet. Es richtet eine HTTP GET-Anforderung ein, indem zuerst die Verbindungs-und Anforderungs Handles der WinHTTP-Sitzung erstellt werden. Der [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) -Befehl gibt den **WinHTTP- \_ \_ Zugriffstyp \_ No \_ Proxy** für die anfängliche Proxykonfiguration an, um anzugeben, dass Anforderungen standardmäßig direkt an den Zielserver gesendet werden. Bei Verwendung von AutoProxy wird die Proxykonfiguration dann direkt auf das Anforderungs handle festgelegt.


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



Im bereitgestellten Beispielcode weist der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Befehl die Funktion an, die automatische Proxy-Konfigurationsdatei automatisch zu ermitteln, indem das Flag für die **\_ \_ automatische \_ Erkennung von WinHTTP AutoProxy** in der [**WinHTTP \_ AutoProxy \_ options**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) -Struktur angegeben wird. Die Verwendung des Flag für die automatische Erkennung von **WinHTTP \_ \_ \_ AutoProxy** erfordert, dass der Code mindestens eine der Flags für die automatische Erkennung angibt (**WinHTTP \_ Auto \_ Detect \_ Type \_ DHCP**, **WinHTTP \_ Auto \_ Detect \_ \_ DNS \_ A**). Der Beispielcode verwendet die Funktion zur automatischen Erkennung von **WinHttpGetProxyForUrl** , da die PAC-URL im Voraus nicht bekannt ist. Wenn in diesem Szenario keine PAC-URL im Netzwerk gefunden werden kann, schlägt **WinHttpGetProxyForUrl** fehl ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen Fehler zurück, wenn die **\_ Automatische WinHTTP- \_ Erkennung \_ fehlgeschlagen** ist).

## <a name="if-the-pac-url-is-known-in-advance"></a>Wenn die PAC-URL im Voraus bekannt ist

Wenn die Anwendung die PAC-URL kennt, kann Sie in der WinHTTP \_ AutoProxy \_ options-Struktur angegeben und [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) konfiguriert werden, um die automatische Erkennungs Phase zu überspringen.

Wenn z. b. eine PAC-Datei im lokalen Netzwerk unter der URL ("") verfügbar ist https://InternalSite/proxy-config.pac , sieht der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Rückruf wie folgt aus:


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



Wenn die [**WinHTTP \_ AutoProxy \_ options**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) -Struktur sowohl **WinHTTP \_ AutoProxy \_ Auto \_ Detect** -als auch **WinHTTP \_ AutoProxy \_ config \_ URL** -Flags angibt (und die Flags für die automatische Ermittlung und eine URL für die automatische Konfiguration angibt), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) versucht zunächst, die automatische Erkennung durchzusetzen, und wenn die automatische Erkennung keine PAC-URL findet, wird auf die von der Anwendung bereitgestellte Auto-config-URL zurückgegriffen.

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Die winhttpdetectautoproxyconfigurl-Funktion

Die [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) -Funktion implementiert eine Teilmenge des WPAD-Protokolls: Sie versucht, die URL für die Datei für die automatische Proxykonfiguration automatisch zu erkennen, ohne die PAC-Datei herunterzuladen oder auszuführen. Diese Funktion ist in speziellen Situationen nützlich, in denen eine Webclient Anwendung das herunterladen und Ausführen der PAC-Datei selbst verarbeiten muss.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Die WinHttpGetIEProxyConfigForCurrentUser-Funktion

Die [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) -Funktion gibt die Internet Explorer-Proxy Einstellungen des aktuellen Benutzers für die aktuelle aktive Netzwerkverbindung zurück, ohne dass ein Aufruf in "WinInet.dll" durchführt. Diese Funktion ist nur nützlich, wenn Sie in einem Prozess aufgerufen wird, der unter einer interaktiven Benutzerkonto Identität ausgeführt wird, da wahrscheinlich keine Internet Explorer-Proxykonfiguration verfügbar ist. Beispielsweise wäre es nicht sinnvoll, diese Funktion über eine ISAPI-DLL aufzurufen, die im IIS-Dienst Prozess ausgeführt wird. Weitere Informationen und ein Szenario, in dem eine WinHTTP-basierte Anwendung **WinHttpGetIEProxyConfigForCurrentUser** verwenden würde, finden Sie unter [Discovery ohne eine Auto-config-Datei](discovery-without-an-auto-config-file.md).

 

 
