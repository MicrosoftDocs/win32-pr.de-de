---
description: Die Send-Methode sendet eine HTTP-Anforderung an einen HTTP-Server.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: IWinHttpRequest::Send-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Send
- WinHttpRequest.Send
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 47155c946d8f49655bf6336a858d2b0752c70caa80f9dd75e0f415ce18ea94c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562940"
---
# <a name="iwinhttprequestsend-method"></a>IWinHttpRequest::Send-Methode

Die **Send-Methode** sendet eine HTTP-Anforderung an einen HTTP-Server.

## <a name="syntax"></a>Syntax


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Text* \[ in, optional\]
</dt> <dd>

Daten, die an den Server gesendet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK,** andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Die zu sendende Anforderung wurde in einem vorherigen Aufruf der [**Open-Methode**](iwinhttprequest-open.md) definiert. Die aufrufende Anwendung kann Daten bereitstellen, die über den *Body-Parameter* an den Server gesendet werden sollen. Wenn das [*HTTP-Verb*](glossary.md) des [**Open-Objekts**](iwinhttprequest-open.md) "GET" ist, sendet diese Methode die Anforderung ohne *Text,* auch wenn sie von der aufrufenden Anwendung bereitgestellt wird.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHttp-Startseite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
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
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print response to console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



Das folgende Skriptbeispiel zeigt, wie sie eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



Das folgende Skriptbeispiel zeigt, wie Daten an einen HTTP-Server gesendet werden.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
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

 

 




