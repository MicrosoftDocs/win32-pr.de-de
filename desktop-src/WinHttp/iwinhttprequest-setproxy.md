---
description: Legt Proxyserverinformationen fest.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: IWinHttpRequest::SetProxy-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: bb85466da6b7492d04bd2e69f4cd51c0c390e9595df13af8d7e6768596771822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562594"
---
# <a name="iwinhttprequestsetproxy-method"></a>IWinHttpRequest::SetProxy-Methode

Die **SetProxy-Methode** legt Proxyserverinformationen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProxySetting* \[ In\]
</dt> <dd>

Die Flags, die diese Methode steuern. Kann einer der folgenden Werte sein.



| Wert                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ DEFAULT</dt> </dl>   | Standardproxyeinstellung. Entspricht **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG</dt> </dl> | Gibt an, dass die Proxyeinstellungen aus der Registrierung ermittelt werden sollen. Dabei wird davon [ ausgegangen,Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) ausgeführt wurde. Wenn Proxycfg.exe nicht ausgeführt wurde und **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG** angegeben ist, entspricht das Verhalten **HTTPREQUEST \_ PROXYSETTING \_ DIRECT**.<br/> |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ DIRECT</dt> </dl>    | Gibt an, dass auf alle HTTP- und HTTPS-Server direkt zugegriffen werden soll. Verwenden Sie diesen Befehl, wenn kein Proxyserver verfügbar ist.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PROXY</dt> </dl>     | Wenn **HTTPREQUEST \_ PROXYSETTING \_ PROXY** angegeben wird, *sollte varProxyServer* auf eine Proxyserverzeichenfolge und *varBypassList* auf eine Domänenumgehungslisten-Zeichenfolge festgelegt werden. Diese Proxykonfiguration gilt nur für die aktuelle Instanz des [**WinHttpRequest-Objekts.**](winhttprequest.md)<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ in, optional\]
</dt> <dd>

Wird auf eine Proxyserverzeichenfolge festgelegt, *wenn ProxySetting* gleich **HTTPREQUEST \_ PROXYSETTING \_ PROXY ist.**

</dd> <dt>

*BypassList* \[ in, optional\]
</dt> <dd>

Wird auf eine Domänenumgehungslisten-Zeichenfolge festgelegt, *wenn ProxySetting* gleich **HTTPREQUEST \_ PROXYSETTING \_ PROXY ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **S \_ OK bei** Erfolg oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Ermöglicht der aufrufenden Anwendung die Angabe der Verwendung von Standardproxyinformationen (konfiguriert durch das Proxykonfigurationstool) oder das Überschreiben [Proxycfg.exe. ](proxycfg-exe--a-proxy-configuration-tool.md) Diese Methode muss aufgerufen werden, bevor die [**Send-Methode aufgerufen**](iwinhttprequest-send.md) wird. Wenn diese Methode nach der [**Send-Methode aufgerufen**](iwinhttprequest-send.md) wird, hat sie keine Auswirkungen.

[**IWinHttpRequest übergibt**](iwinhttprequest-interface.md) diese Parameter an Microsoft Windows HTTP Services (WinHTTP).

> [!Note]  
> Informationen Windows XP und Windows 2000 finden Sie im Abschnitt Laufzeitanforderungen der [WinHTTP-Startseite.](winhttp-start-page.md)

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie die Proxyeinstellungen für einen bestimmten Proxyserver festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen. Dieses Beispiel muss über eine Eingabeaufforderung ausgeführt werden. Diese Proxyeinstellungen funktionieren nur, wenn Sie über einen Proxyserver mit dem Namen "Proxyserver" verfügen, der Port 80 verwendet, und Ihr Computer den Proxyserver umgehen kann, wenn der Hostname mit \_ ".microsoft.com" endet.


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
        }
    if (SUCCEEDED(hr))
    {   // Open WinHttpRequest.
            BSTR bstrMethod  = SysAllocString(L"GET");
                BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
                SysFreeString(bstrMethod);
                SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
                hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



Das folgende Skriptbeispiel zeigt, wie Sie die Proxyeinstellungen für einen bestimmten Proxyserver festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen. Diese Proxyeinstellungen funktionieren nur, wenn Sie über einen Proxyserver mit dem Namen "Proxyserver" verfügen, der Port 80 verwendet, und Ihr Computer den Proxyserver umgehen kann, wenn der Hostname mit \_ ".microsoft.com" endet.


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




