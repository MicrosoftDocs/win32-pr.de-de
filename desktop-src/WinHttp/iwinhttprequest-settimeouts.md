---
description: Die settimeouts-Methode gibt die einzelnen Timeout Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'Iwinhttprequest:: settimeouts-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219415"
---
# <a name="iwinhttprequestsettimeouts-method"></a>Iwinhttprequest:: settimeouts-Methode

Die **settimeouts** -Methode gibt die einzelnen Timeout Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Resolvetimeout* \[ in\]
</dt> <dd>

Timeout Wert, der beim Auflösen eines Host namens (z. b. `www.microsoft.com` ) in eine IP-Adresse (z. b. 192.168.131.199) in Millisekunden angewendet wurde. Der Standardwert ist 0 (null), was bedeutet, dass kein Timeout (unendlich) auftritt. Wenn das DNS-Timeout mithilfe \_ des Namens Auflösungs \_ Timeouts angegeben wird, entsteht ein mehr Aufwand von einem Thread pro Anforderung.

</dd> <dt>

*ConnectTimeout* \[ in\]
</dt> <dd>

Timeout Wert, der beim Einrichten eines Kommunikations Sockets mit dem Zielserver (in Millisekunden) angewendet wurde. Der Standardwert ist 60.000 (60 Sekunden).

</dd> <dt>

*SendTimeout* \[ in\]
</dt> <dd>

Timeout Wert, der beim Senden eines einzelnen Pakets mit Anforderungs Daten auf dem Kommunikations Socket an den Zielserver (in Millisekunden) angewendet wird. Eine große Anforderung, die an einen HTTP-Server gesendet wird, wird normalerweise in mehrere Pakete aufgeteilt. das Sende Timeout gilt für das einzelne Senden der einzelnen Pakete. Der Standardwert ist 30.000 (30 Sekunden).

</dd> <dt>

*ReceiveTimeout* \[ in\]
</dt> <dd>

Timeout Wert, der beim Empfangen eines Pakets mit Antwortdaten vom Zielserver in Millisekunden angewendet wurde. Große Antworten werden in mehrere Pakete aufgeteilt. der Empfangs Timeout bezieht sich auf das Abrufen der einzelnen Datenpakete vom Socket. Der Standardwert ist 30.000 (30 Sekunden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Alle Parameter sind erforderlich. Mit dem Wert 0 oder-1 wird ein Timeout festgelegt, um unendlich zu warten. Ein Wert größer 0 (null) legt den Timeout Wert in Millisekunden fest. Beispielsweise würde 30.000 das Timeout auf 30 Sekunden festlegen. Alle negativen Werte, mit Ausnahme von-1, führen dazu, dass diese Methode fehlschlägt.

Timeout Werte werden auf der Winsock-Ebene angewendet.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie alle WinHTTP-Timeouts auf 30 Sekunden festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.


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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
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



Im folgenden Skript Beispiel wird gezeigt, wie alle WinHTTP-Timeouts auf 30 Sekunden festgelegt werden, eine HTTP-Verbindung geöffnet und eine HTTP-Anforderung gesendet wird.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

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

 

 




