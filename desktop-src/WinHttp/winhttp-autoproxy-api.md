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
# <a name="winhttp-autoproxy-functions"></a><span data-ttu-id="10e99-103">WinHTTP AutoProxy-Funktionen</span><span class="sxs-lookup"><span data-stu-id="10e99-103">WinHTTP AutoProxy Functions</span></span>

<span data-ttu-id="10e99-104">WinHTTP implementiert das WPAD-Protokoll mithilfe der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion zusammen mit zwei unterstützenden Hilfsprogrammfunktionen, [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) und [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span><span class="sxs-lookup"><span data-stu-id="10e99-104">WinHTTP implements the WPAD protocol using the [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function along with two supporting utility functions, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) and [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span></span>

<span data-ttu-id="10e99-105">Die AutoProxy-Unterstützung ist nicht vollständig in den HTTP-Stapel in WinHTTP integriert.</span><span class="sxs-lookup"><span data-stu-id="10e99-105">AutoProxy support is not fully integrated into the HTTP stack in WinHTTP.</span></span> <span data-ttu-id="10e99-106">Bevor eine Anforderung gesendet wird, muss die Anwendung [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) aufrufen, um den Namen eines Proxy Servers zu erhalten, und dann [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mithilfe des **WinHTTP- \_ options \_ Proxys** aufrufen, um die Proxykonfiguration für das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellte WinHTTP-Anforderungs Handle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="10e99-106">Before sending a request, the application must call [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to obtain the name of a proxy server and then call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) using **WINHTTP\_OPTION\_PROXY** to set the proxy configuration on the WinHTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span>

<span data-ttu-id="10e99-107">Die [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion kann alle drei Schritte des WPAD-Protokolls ausführen, das in der vorherigen Übersicht beschrieben wurde: (1) ermitteln der PAC-URL, (2) laden Sie die PAC-Skriptdatei herunter, (3) führen Sie den Skriptcode aus, und geben Sie die Proxykonfiguration in einer **WinHTTP- \_ Proxy \_ Informations** Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="10e99-107">The [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function can execute all three steps of the WPAD protocol described in the previous overview: (1) discover the PAC URL, (2) download the PAC script file, (3) execute the script code and return the proxy configuration in a **WINHTTP\_PROXY\_INFO** structure.</span></span> <span data-ttu-id="10e99-108">Wenn die Anwendung im Voraus die PAC-URL kennt, kann Sie diese als " **WinHttpGetProxyForUrl**" angeben.</span><span class="sxs-lookup"><span data-stu-id="10e99-108">Optionally, if the application knows in advance the PAC URL it can specify this to **WinHttpGetProxyForUrl**.</span></span>

<span data-ttu-id="10e99-109">Im folgenden Beispielcode wird AutoProxy verwendet.</span><span class="sxs-lookup"><span data-stu-id="10e99-109">The following example code uses autoproxy.</span></span> <span data-ttu-id="10e99-110">Es richtet eine HTTP GET-Anforderung ein, indem zuerst die Verbindungs-und Anforderungs Handles der WinHTTP-Sitzung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="10e99-110">It sets up an HTTP GET request by first creating the WinHTTP session connect and request handles.</span></span> <span data-ttu-id="10e99-111">Der [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) -Befehl gibt den **WinHTTP- \_ \_ Zugriffstyp \_ No \_ Proxy** für die anfängliche Proxykonfiguration an, um anzugeben, dass Anforderungen standardmäßig direkt an den Zielserver gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="10e99-111">The [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) call specifies **WINHTTP\_ACCESS\_TYPE\_NO\_PROXY** for the initial proxy configuration, to indicate that requests are sent directly to the target server by default.</span></span> <span data-ttu-id="10e99-112">Bei Verwendung von AutoProxy wird die Proxykonfiguration dann direkt auf das Anforderungs handle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="10e99-112">Using autoproxy, it then sets the proxy configuration directly on the request handle.</span></span>


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



<span data-ttu-id="10e99-113">Im bereitgestellten Beispielcode weist der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Befehl die Funktion an, die automatische Proxy-Konfigurationsdatei automatisch zu ermitteln, indem das Flag für die **\_ \_ automatische \_ Erkennung von WinHTTP AutoProxy** in der [**WinHTTP \_ AutoProxy \_ options**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10e99-113">In the provided example code, the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instructs the function to discover the proxy auto-config file automatically by specifying the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag in the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure.</span></span> <span data-ttu-id="10e99-114">Die Verwendung des Flag für die automatische Erkennung von **WinHTTP \_ \_ \_ AutoProxy** erfordert, dass der Code mindestens eine der Flags für die automatische Erkennung angibt (**WinHTTP \_ Auto \_ Detect \_ Type \_ DHCP**, **WinHTTP \_ Auto \_ Detect \_ \_ DNS \_ A**).</span><span class="sxs-lookup"><span data-stu-id="10e99-114">Use of the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag requires the code to specify one or both of the auto-detection flags (**WINHTTP\_AUTO\_DETECT\_TYPE\_DHCP**, **WINHTTP\_AUTO\_DETECT\_TYPE\_DNS\_A**).</span></span> <span data-ttu-id="10e99-115">Der Beispielcode verwendet die Funktion zur automatischen Erkennung von **WinHttpGetProxyForUrl** , da die PAC-URL im Voraus nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="10e99-115">The example code uses the auto-detection feature of **WinHttpGetProxyForUrl** because the PAC URL is not known in advance.</span></span> <span data-ttu-id="10e99-116">Wenn in diesem Szenario keine PAC-URL im Netzwerk gefunden werden kann, schlägt **WinHttpGetProxyForUrl** fehl ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen Fehler zurück, wenn die **\_ Automatische WinHTTP- \_ Erkennung \_ fehlgeschlagen** ist).</span><span class="sxs-lookup"><span data-stu-id="10e99-116">If a PAC URL cannot be located on the network in this scenario, **WinHttpGetProxyForUrl** fails ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_WINHTTP\_AUTODETECTION\_FAILED**).</span></span>

## <a name="if-the-pac-url-is-known-in-advance"></a><span data-ttu-id="10e99-117">Wenn die PAC-URL im Voraus bekannt ist</span><span class="sxs-lookup"><span data-stu-id="10e99-117">If the PAC URL is Known in Advance</span></span>

<span data-ttu-id="10e99-118">Wenn die Anwendung die PAC-URL kennt, kann Sie in der WinHTTP \_ AutoProxy \_ options-Struktur angegeben und [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) konfiguriert werden, um die automatische Erkennungs Phase zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="10e99-118">If the application does know the PAC URL, it can specify it in the WINHTTP\_AUTOPROXY\_OPTIONS structure and configure [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to skip the auto-detection phase.</span></span>

<span data-ttu-id="10e99-119">Wenn z. b. eine PAC-Datei im lokalen Netzwerk unter der URL ("") verfügbar ist https://InternalSite/proxy-config.pac , sieht der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Rückruf wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="10e99-119">For example, if a PAC file is available on the local network at the URL, "https://InternalSite/proxy-config.pac", the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) would look the following.</span></span>


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



<span data-ttu-id="10e99-120">Wenn die [**WinHTTP \_ AutoProxy \_ options**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) -Struktur sowohl **WinHTTP \_ AutoProxy \_ Auto \_ Detect** -als auch **WinHTTP \_ AutoProxy \_ config \_ URL** -Flags angibt (und die Flags für die automatische Ermittlung und eine URL für die automatische Konfiguration angibt), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) versucht zunächst, die automatische Erkennung durchzusetzen, und wenn die automatische Erkennung keine PAC-URL findet, wird auf die von der Anwendung bereitgestellte Auto-config-URL zurückgegriffen.</span><span class="sxs-lookup"><span data-stu-id="10e99-120">If the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure specifies both **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** and **WINHTTP\_AUTOPROXY\_CONFIG\_URL** flags (and specifies auto-detction flags and an auto-config URL), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) first attempts auto-detection, and then, if auto-detection fails to locate a PAC URL, "falls back" to the auto-config URL supplied by the application.</span></span>

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a><span data-ttu-id="10e99-121">Die winhttpdetectautoproxyconfigurl-Funktion</span><span class="sxs-lookup"><span data-stu-id="10e99-121">The WinHttpDetectAutoProxyConfigUrl Function</span></span>

<span data-ttu-id="10e99-122">Die [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) -Funktion implementiert eine Teilmenge des WPAD-Protokolls: Sie versucht, die URL für die Datei für die automatische Proxykonfiguration automatisch zu erkennen, ohne die PAC-Datei herunterzuladen oder auszuführen.</span><span class="sxs-lookup"><span data-stu-id="10e99-122">The [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) function implements a subset of the WPAD protocol: it attempts to auto-detect the URL for the proxy auto-config file, without downloading or executing the PAC file.</span></span> <span data-ttu-id="10e99-123">Diese Funktion ist in speziellen Situationen nützlich, in denen eine Webclient Anwendung das herunterladen und Ausführen der PAC-Datei selbst verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="10e99-123">This function is useful in special situations where a Web client application must handle the download and execution of the PAC file itself.</span></span>

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a><span data-ttu-id="10e99-124">Die WinHttpGetIEProxyConfigForCurrentUser-Funktion</span><span class="sxs-lookup"><span data-stu-id="10e99-124">The WinHttpGetIEProxyConfigForCurrentUser Function</span></span>

<span data-ttu-id="10e99-125">Die [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) -Funktion gibt die Internet Explorer-Proxy Einstellungen des aktuellen Benutzers für die aktuelle aktive Netzwerkverbindung zurück, ohne dass ein Aufruf in "WinInet.dll" durchführt.</span><span class="sxs-lookup"><span data-stu-id="10e99-125">The [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) function returns the current user Internet Explorer proxy settings for the current active network connection, without calling into "WinInet.dll".</span></span> <span data-ttu-id="10e99-126">Diese Funktion ist nur nützlich, wenn Sie in einem Prozess aufgerufen wird, der unter einer interaktiven Benutzerkonto Identität ausgeführt wird, da wahrscheinlich keine Internet Explorer-Proxykonfiguration verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="10e99-126">This function is only useful when called within a process that is running under an interactive user account identity, because no Internet Explorer proxy configuration is likely to be available otherwise.</span></span> <span data-ttu-id="10e99-127">Beispielsweise wäre es nicht sinnvoll, diese Funktion über eine ISAPI-DLL aufzurufen, die im IIS-Dienst Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10e99-127">For example, it would not be useful to call this function from an ISAPI DLL running in the IIS service process.</span></span> <span data-ttu-id="10e99-128">Weitere Informationen und ein Szenario, in dem eine WinHTTP-basierte Anwendung **WinHttpGetIEProxyConfigForCurrentUser** verwenden würde, finden Sie unter [Discovery ohne eine Auto-config-Datei](discovery-without-an-auto-config-file.md).</span><span class="sxs-lookup"><span data-stu-id="10e99-128">For more information and a scenario in which a WinHTTP-based application would use **WinHttpGetIEProxyConfigForCurrentUser**, see [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).</span></span>

 

 
