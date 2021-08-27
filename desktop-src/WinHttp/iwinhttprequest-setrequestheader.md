---
description: Fügt einen HTTP-Anforderungsheader hinzu, ändert oder löscht ihn.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: IWinHttpRequest::SetRequestHeader-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 1f6db5ef09a0eca56fec8101d710c62eb5165742d47e3961593f38d4a59851ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052028"
---
# <a name="iwinhttprequestsetrequestheader-method"></a>IWinHttpRequest::SetRequestHeader-Methode

Die **SetRequestHeader-Methode** fügt einen HTTP-Anforderungsheader hinzu, ändert oder löscht ihn.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Header* \[ In\]
</dt> <dd>

Gibt den Namen des headers an, der festgelegt werden soll, z. B. "depth". Dieser Parameter sollte keinen Doppelpunkt enthalten und muss der tatsächliche Text des HTTP-Headers sein.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Gibt den Wert des Headers an, z. B. "infinity".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **S \_ OK bei** Erfolg oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Header werden über Umleitungen übertragen. Dies kann zu einem Sicherheitsrisiko werden. Um zu vermeiden, dass Header übertragen werden, wenn eine Umleitung auftritt, verwenden Sie den [*WINHTTP \_ STATUS \_ CALLBACK-Rückruf,*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) um die spezifischen Header zu korrigieren, wenn eine Umleitung auftritt.

Mit **der SetRequestHeader-Methode** kann die aufrufende Anwendung vor dem Senden der Anforderung einen HTTP-Anforderungsheader hinzufügen oder löschen. Der Headername wird in *Header angegeben,* und das Headertoken oder der Wert wird in *Wert angegeben.* Um einen Header hinzuzufügen, geben Sie einen Headernamen und -wert an. Wenn bereits ein anderer Header mit diesem Namen vorhanden ist, wird er ersetzt. Um einen Header zu löschen, legen *Sie Header* auf den Namen des zu löschenden Headers und *Value auf* **NULL fest.**

Der Name und Wert von Anforderungsheadern, die mit dieser Methode hinzugefügt wurden, werden überprüft. Header müssen wohlgeformt sein. Weitere Informationen zu gültigen HTTP-Headern finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Wenn ein ungültiger Header verwendet wird, tritt ein Fehler auf, und der Header wird nicht hinzugefügt.

> [!Note]  
> Informationen Windows XP und Windows 2000 finden [](winhttp-start-page.md) Sie im Abschnitt Laufzeitanforderungen der WinHTTP-Startseite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, einen Anforderungsheader festlegen, eine HTTP-Anforderung senden und den Antworttext lesen. Dieses Beispiel muss über eine Eingabeaufforderung ausgeführt werden.


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
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
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



Das folgende Skriptbeispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, einen Anforderungsheader festlegen und eine HTTP-Anforderung senden.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

