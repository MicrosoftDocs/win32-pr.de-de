---
description: Legt Anmeldeinformationen fest, die mit einem HTTP-Server verwendet werden sollen, unabhängig davon, ob es sich um einen Proxyserver oder einen Ursprungsserver handelt.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: IWinHttpRequest::SetCredentials-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9246352e78472461bfbfe37569d9bd631905fda03c87571ed7ed3dad04edb797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744466"
---
# <a name="iwinhttprequestsetcredentials-method"></a>IWinHttpRequest::SetCredentials-Methode

Die **SetCredentials-Methode** legt Anmeldeinformationen fest, die mit einem HTTP-Server verwendet werden sollen, unabhängig davon, ob es sich um einen Proxyserver oder einen Ursprungsserver handelt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserName* \[ In\]
</dt> <dd>

Gibt den Benutzernamen für die Authentifizierung an.

</dd> <dt>

*Kennwort* \[ In\]
</dt> <dd>

Gibt das Kennwort für die Authentifizierung an. Dieser Parameter wird ignoriert, wenn *bstrUserName* **NULL ist** oder fehlt.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Gibt an, wann [**IWinHttpRequest Anmeldeinformationen**](iwinhttprequest-interface.md) verwendet. Kann einer der folgenden Werte sein.



| Wert                                                                                                               | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ SETCREDENTIALS \_ FÜR \_ SERVER</dt> </dl> | Anmeldeinformationen werden an einen Server übergeben.<br/> |
| <dl> <dt>HTTPREQUEST \_ SETCREDENTIALS \_ FÜR \_ PROXY</dt> </dl>  | Anmeldeinformationen werden an einen Proxy übergeben.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **S \_ OK bei** Erfolg oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Diese Methode gibt einen Fehlerwert zurück, wenn ein Aufruf von [**Open**](iwinhttprequest-open.md) nicht erfolgreich abgeschlossen wurde. Es wird davon ausgegangen, dass ein gewisses Maß an Interaktion mit einem Proxy- oder Ursprungsserver erfolgen muss, bevor Benutzer Anmeldeinformationen für die Sitzung festlegen können. Darüber hinaus können Benutzer die Anmeldeinformationen erst formatieren, wenn sie wissen, welche Authentifizierungsschemas unterstützt werden.

> [!Note]  
> Informationen Windows XP und Windows 2000 finden [](winhttp-start-page.md) Sie im Abschnitt Laufzeitanforderungen der WinHTTP-Startseite.

 

Um sich sowohl beim Server als auch beim Proxy zu authentifizieren, muss die Anwendung **SetCredentials zweimal** aufrufen. zuerst mit dem *Flags-Parameter,* der auf **HTTPREQUEST \_ SETCREDENTIALS \_ FOR \_ SERVER** festgelegt ist, und dem zweiten Parameter, bei dem der *Flags-Parameter* auf **HTTPREQUEST \_ SETCREDENTIALS \_ FOR PROXY festgelegt \_ ist.**

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, Anmeldeinformationen für den Server festlegen, eine HTTP-Anforderung senden und den Antworttext lesen. Dieses Beispiel muss über eine Eingabeaufforderung ausgeführt werden.


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

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



Das folgende Skriptbeispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, Anmeldeinformationen für den Server festlegen, Anmeldeinformationen für einen Proxy festlegen, sofern einer verwendet wird, eine HTTP-Anforderung senden und den Antworttext lesen.


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




