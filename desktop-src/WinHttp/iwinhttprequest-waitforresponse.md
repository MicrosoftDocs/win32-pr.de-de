---
description: Die WaitForResponse-Methode wartet auf den Abschluss einer asynchronen Sende Methode mit optionalem Timeout Wert (in Sekunden).
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'Iwinhttprequest:: WaitForResponse-Methode'
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
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350070"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>Iwinhttprequest:: WaitForResponse-Methode

Die **WaitForResponse** -Methode wartet auf den Abschluss einer asynchronen [**Sende**](iwinhttprequest-send.md) Methode mit optionalem Timeout Wert (in Sekunden).

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

Timeout Wert in Sekunden. Das Standard Timeout ist unendlich. Wenn Sie das Timeout explizit auf unendlich festlegen möchten, verwenden Sie den Wert-1.

</dd> <dt>

*Erfolgreich* \[ Out, retval\]
</dt> <dd>

Empfängt einen der folgenden Werte.



| Wert                                                                                                                                                         | Bedeutung                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**Variant \_ true**</dt> </dl>    | Eine Antwort wurde empfangen.<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**Variant \_ false**</dt> </dl> | Der angegebene Timeout Zeitraum wurde überschritten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Diese Methode hält die Ausführung an und wartet auf eine Antwort auf eine asynchrone Anforderung. Diese Methode sollte nach einem [**Send**](iwinhttprequest-send.md)-Vorgang aufgerufen werden. Beim Aufrufen von Anwendungen kann ein optionaler *Timeout* Wert (in Sekunden) angegeben werden. Wenn für diese Methode ein Timeout auftritt, wird die Anforderung nicht abgebrochen. Auf diese Weise kann die aufrufende Anwendung in einem nachfolgenden Aufruf dieser Methode weiterhin auf die Anforderung warten.

Das Aufrufen dieser Eigenschaft nach einer synchronen [**Send**](iwinhttprequest-send.md) -Methode wird sofort zurückgegeben und hat keine Auswirkungen.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

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



Im folgenden Skript Beispiel wird gezeigt, wie eine asynchrone HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet, auf eine Antwort gewartet und der Antworttext gelesen wird.


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

[**Eren**](iwinhttprequest-open.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




