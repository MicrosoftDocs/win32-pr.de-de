---
description: Legt Proxy Server Informationen fest.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'Iwinhttprequest:: SetProxy-Methode'
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
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352602"
---
# <a name="iwinhttprequestsetproxy-method"></a>Iwinhttprequest:: SetProxy-Methode

Die **SetProxy** -Methode legt Proxy Server Informationen fest.

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

*Proxysetting* \[ in\]
</dt> <dd>

Die Flags, die diese Methode steuern. Kann einen der folgenden Werte aufweisen.



| Wert                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HttpRequest \_ proxysetting \_ Standard</dt> </dl>   | Standard Proxy Einstellung. Äquivalent zu **HttpRequest \_ proxysetting \_ preconfig**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>HttpRequest \_ proxysetting \_ preconfig</dt> </dl> | Gibt an, dass die Proxy Einstellungen aus der Registrierung abgerufen werden sollen. Dabei wird davon ausgegangen, dass [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) ausgeführt wurde. Wenn Proxycfg.exe nicht ausgeführt wurde und **HttpRequest \_ proxysetting \_ preconfig** angegeben ist, entspricht das Verhalten dem **HttpRequest \_ proxysetting \_ Direct**.<br/> |
| <dl> <dt>HttpRequest \_ proxysetting \_ Direct</dt> </dl>    | Gibt an, dass direkt auf alle HTTP-und HTTPS-Server zugegriffen werden soll. Verwenden Sie diesen Befehl, wenn kein Proxy Server vorhanden ist.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>HttpRequest \_ proxysetting- \_ Proxy</dt> </dl>     | Wenn **HttpRequest \_ proxysetting \_ Proxy** angegeben ist, muss *varproxyserver* auf eine Proxy Server Zeichenfolge festgelegt werden, und *varbypasslist* sollte auf eine Domänen Umgehungs Listen-Zeichenfolge festgelegt werden. Diese Proxykonfiguration gilt nur für die aktuelle Instanz des [**WinHttpRequest**](winhttprequest.md) -Objekts.<br/>                                    |



 

</dd> <dt>

*Proxy Server* \[ in, optional\]
</dt> <dd>

Legen Sie auf eine Proxy Server Zeichenfolge fest, wenn *proxysetting* dem **HttpRequest \_ proxysetting- \_ Proxy** entspricht.

</dd> <dt>

*BypassList* \[ in, optional\]
</dt> <dd>

Festlegen auf eine Domänen Umgehungs Listen-Zeichenfolge, wenn *proxysetting* dem **HttpRequest \_ proxysetting- \_ Proxy** entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Ermöglicht es der aufrufenden Anwendung, die Verwendung von Standard Proxy Informationen (konfiguriert durch das Proxy Konfigurationstool) oder das Überschreiben von [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md)anzugeben. Diese Methode muss aufgerufen werden, bevor die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wird. Wenn diese Methode nach der [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wird, hat Sie keine Auswirkungen.

[**Iwinhttprequest**](iwinhttprequest-interface.md) übergibt diese Parameter an Microsoft Windows HTTP-Dienste (WinHTTP).

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie die Proxy Einstellungen für einen bestimmten Proxy Server festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen. Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden. Diese Proxy Einstellungen funktionieren nur, wenn Sie über einen Proxy Server mit dem Namen "Proxy \_ Server" verfügen, der Port 80 verwendet, und der Computer den Proxy Server umgehen kann, wenn der Hostname auf ". Microsoft.com" endet.


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



Das folgende Beispielskript zeigt, wie Sie die Proxy Einstellungen für einen bestimmten Proxy Server festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen. Diese Proxy Einstellungen funktionieren nur, wenn Sie über einen Proxy Server mit dem Namen "Proxy \_ Server" verfügen, der Port 80 verwendet, und der Computer den Proxy Server umgehen kann, wenn der Hostname auf ". Microsoft.com" endet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwinhttprequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




