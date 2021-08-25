---
description: WinHTTP implementiert das WPAD-Protokoll mithilfe der WinHttpGetProxyForUrl-Funktion zusammen mit zwei unterstützenden Hilfsfunktionen, WinHttpDetectAutoProxyConfigUrl und WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: WinHTTP AutoProxy-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955710"
---
# <a name="winhttp-autoproxy-functions"></a>WinHTTP AutoProxy-Funktionen

WinHTTP implementiert das WPAD-Protokoll mithilfe der [**WinHttpGetProxyForUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) zusammen mit zwei unterstützenden Hilfsfunktionen: [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) und [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

Die AutoProxy-Unterstützung ist nicht vollständig in den HTTP-Stapel in WinHTTP integriert. Vor dem Senden einer Anforderung muss die Anwendung [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) aufrufen, um den Namen eines Proxyservers zu erhalten, und dann [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit **WINHTTP \_ OPTION \_ PROXY** aufrufen, um die Proxykonfiguration für das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellte WinHTTP-Anforderungshandle festlegen zu können.

Die [**WinHttpGetProxyForUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) kann alle drei Schritte des in der vorherigen Übersicht beschriebenen WPAD-Protokolls ausführen: (1) Die PAC-URL finden Sie, (2) laden Sie die PAC-Skriptdatei herunter, (3) führen Sie den Skriptcode aus, und geben Sie die Proxykonfiguration in einer **WINHTTP PROXY \_ \_ INFO-Struktur** zurück. Wenn die Anwendung die PAC-URL im Voraus kennt, kann sie diese optional für **WinHttpGetProxyForUrl angeben.**

Im folgenden Beispielcode wird autoproxy verwendet. Sie richtet eine HTTP GET-Anforderung ein, indem zuerst die WinHTTP-Sitzungs-Verbindungs- und Anforderungshandles erstellt werden. Der [**WinHttpOpen-Aufruf**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) gibt **WINHTTP \_ ACCESS TYPE NO \_ \_ \_ PROXY** für die anfängliche Proxykonfiguration an, um anzugeben, dass Anforderungen standardmäßig direkt an den Zielserver gesendet werden. Mithilfe des automatischen Proxys wird dann die Proxykonfiguration direkt auf dem Anforderungshand handle fest.


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



Im bereitgestellten Beispielcode weist der Aufruf von [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) die Funktion an, die automatische Proxykonfigurationsdatei automatisch zu ermitteln, indem das **WINHTTP \_ AUTOPROXY \_ AUTO \_ DETECT-Flag** in der [**WINHTTP \_ AUTOPROXY \_ OPTIONS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) angegeben wird. Bei Verwendung des **WINHTTP \_ AUTOPROXY \_ AUTO \_ DETECT-Flags** muss der Code eines oder beide der Flags für die automatische Erkennung angeben (**WINHTTP AUTO DETECT TYPE \_ \_ \_ \_ DHCP**, **WINHTTP AUTO DETECT TYPE \_ DNS \_ \_ \_ \_ A**). Im Beispielcode wird das Feature für die automatische Erkennung von **WinHttpGetProxyForUrl** verwendet, da die PAC-URL im Voraus nicht bekannt ist. Wenn in diesem Szenario keine PAC-URL im Netzwerk gefunden werden kann, schlägt **WinHttpGetProxyForUrl** fehl ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR \_ WINHTTP \_ AUTODETECTION \_ FAILED zurück).**

## <a name="if-the-pac-url-is-known-in-advance"></a>Wenn die PAC-URL im Voraus bekannt ist

Wenn die Anwendung die PAC-URL nicht kennt, kann sie sie in der WINHTTP AUTOPROXY OPTIONS-Struktur angeben und \_ \_ [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) so konfigurieren, dass die Automatische Erkennungsphase übersprungen wird.

Wenn beispielsweise eine PAC-Datei im lokalen Netzwerk unter der URL " " verfügbar ist, sieht der Aufruf von https://InternalSite/proxy-config.pac [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) wie folgt aus.


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



Wenn die [**WINHTTP \_ AUTOPROXY \_ OPTIONS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) sowohl **WINHTTP \_ AUTOPROXY \_ AUTO \_ DETECT-** als auch **WINHTTP \_ AUTOPROXY \_ CONFIG-URL-Flags \_** angibt (und automatische Detction-Flags und eine AUTOCONFIG-URL angibt), versucht [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) zunächst die automatische Erkennung. Wenn bei der automatischen Erkennung keine PAC-URL gefunden werden kann, wird auf die von der Anwendung bereitgestellte URL für die automatische Konfiguration "zurückgeführt".

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Die WinHttpDetectAutoProxyConfigUrl-Funktion

Die [**WinHttpDetectAutoProxyConfigUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementiert eine Teilmenge des WPAD-Protokolls: Sie versucht, die URL für die automatische Proxykonfigurationsdatei automatisch zu erkennen, ohne die PAC-Datei herunterzuladen oder ausführen zu müssen. Diese Funktion ist in besonderen Situationen nützlich, in denen eine Webclientanwendung den Download und die Ausführung der PAC-Datei selbst verarbeiten muss.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Die WinHttpGetIEProxyConfigForCurrentUser-Funktion

Die [**WinHttpGetIEProxyConfigForCurrentUser-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) gibt die aktuellen Internet Explorer-Proxyeinstellungen für die aktuelle aktive Netzwerkverbindung zurück, ohne "WinInet.dll". Diese Funktion ist nur nützlich, wenn sie innerhalb eines Prozesses aufgerufen wird, der unter einer interaktiven Benutzerkontoidentität ausgeführt wird, da andernfalls wahrscheinlich keine Internet Explorer Proxykonfiguration verfügbar ist. Beispielsweise wäre es nicht sinnvoll, diese Funktion von einer ISAPI-DLL auf die im IIS-Dienstprozess ausgeführt wird. Weitere Informationen und ein Szenario, in dem eine WinHTTP-basierte Anwendung **WinHttpGetIEProxyConfigForCurrentUser** verwenden würde, finden Sie unter [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).

 

 
