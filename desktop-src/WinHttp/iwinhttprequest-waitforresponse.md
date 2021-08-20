---
description: Die WaitForResponse-Methode wartet in Sekunden, bis eine asynchrone Send-Methode mit einem optionalen Time out-Wert abgeschlossen ist.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: IWinHttpRequest::WaitForResponse-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: e4f72edf2a3532c6d0f2641d979885e6d294c2ad923a28f19b71b348ea3a6377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051998"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>IWinHttpRequest::WaitForResponse-Methode

Die **WaitForResponse-Methode** wartet in Sekunden, bis eine asynchrone [**Send-Methode**](iwinhttprequest-send.md) mit einem optionalen Time out-Wert abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timeout* \[ in, optional\]
</dt> <dd>

Time out-Wert in Sekunden. Das Standardtime out ist unendlich. Um time-out explizit auf unendlich festzulegen, verwenden Sie den Wert -1.

</dd> <dt>

*Erfolgreich* \[ out, retval\]
</dt> <dd>

Empfängt einen der folgenden Werte.



| Wert                                                                                                                                                         | Bedeutung                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**VARIANT \_ TRUE**</dt> </dl>    | Eine Antwort wurde empfangen.<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**VARIANT \_ FALSE**</dt> </dl> | Der angegebene Time out-Zeitraum wurde überschritten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK,** andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Diese Methode unterbricht die Ausführung, während auf eine Antwort auf eine asynchrone Anforderung gewartet wird. Diese Methode sollte nach einer [**Send-Methode**](iwinhttprequest-send.md)aufgerufen werden. Aufrufende Anwendungen können einen optionalen *Timeoutwert* in Sekunden angeben. Wenn für diese Methode ein Zeitabbruch erfolgt, wird die Anforderung nicht abgebrochen. Auf diese Weise kann die aufrufende Anwendung bei Bedarf in einem nachfolgenden Aufruf dieser Methode weiterhin auf die Anforderung warten.

Der Aufruf dieser Eigenschaft nach einer synchronen [**Send-Methode**](iwinhttprequest-send.md) wird sofort zurückgegeben und hat keine Auswirkungen.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHTTP-Startseite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine asynchrone HTTP-Verbindung öffnen, eine HTTP-Anforderung senden, auf die Antwort warten und den Antworttext lesen.


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
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
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



Das folgende Skriptbeispiel zeigt, wie Sie eine asynchrone HTTP-Verbindung öffnen, eine HTTP-Anforderung senden, auf eine Antwort warten und den Antworttext lesen.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**Öffnen**](iwinhttprequest-open.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




