---
description: Fügt einen HTTP-Anforderungs Header hinzu, ändert oder löscht ihn.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: 'Iwinhttprequest:: ltrequestheader-Methode'
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
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363798"
---
# <a name="iwinhttprequestsetrequestheader-method"></a>Iwinhttprequest:: ltrequestheader-Methode

Mit der Methode " **ltrequestheader** " wird ein HTTP-Anforderungs Header hinzugefügt, geändert oder gelöscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Header* \[ in\]
</dt> <dd>

Gibt den Namen des festzulegenden Headers an, z. b. "Tiefe". Dieser Parameter darf keinen Doppelpunkt enthalten und muss den eigentlichen Text des HTTP-Headers enthalten.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Gibt den Wert des Headers an, z. b. "unendlich".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Header werden über Umleitungen übertragen. Dies kann zu einem Sicherheitsrisiko führen. Um zu vermeiden, dass Header bei einer Umleitung übertragen werden, korrigieren Sie mithilfe des [*WinHTTP- \_ Status \_ Rückruf*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) Rückrufs die spezifischen Header, wenn eine Umleitung erfolgt.

Mit der **setrequestheader** -Methode kann die aufrufende Anwendung einen HTTP-Anforderungs Header vor dem Senden der Anforderung hinzufügen oder löschen. Der Header Name wird in der *Kopfzeile* angegeben, und das Header Token oder der Wert wird als *Wert* angegeben. Um einen Header hinzuzufügen, geben Sie einen Header Namen und einen Wert an. Wenn eine andere Kopfzeile mit diesem Namen bereits vorhanden ist, wird Sie ersetzt. Zum Löschen eines Headers legen Sie den *Header* auf den Namen des zu löschenden Headers fest, und legen Sie den *Wert* auf **null** fest.

Der Name und der Wert der Anforderungs Header, die mit dieser Methode hinzugefügt werden, werden überprüft. Header müssen wohl geformt sein. Weitere Informationen zu gültigen HTTP-Headern finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Wenn ein ungültiger Header verwendet wird, tritt ein Fehler auf, und der Header wird nicht hinzugefügt.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, einen Anforderungs Header festlegen, eine HTTP-Anforderung senden und den Antworttext lesen. Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.


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



Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, ein Anforderungs Header festgelegt und eine HTTP-Anforderung gesendet wird.


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

 

