---
description: Die SetTimeouts-Methode gibt die einzelnen Timeoutkomponenten eines Sende-/Empfangsvorgangs in Millisekunden an.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: IWinHttpRequest::SetTimeouts-Methode
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
ms.openlocfilehash: e31fbe80f106735a43126b2be5181478b932e2f813b207984959cf013d3fd752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562455"
---
# <a name="iwinhttprequestsettimeouts-method"></a>IWinHttpRequest::SetTimeouts-Methode

Die **SetTimeouts-Methode** gibt die einzelnen Timeoutkomponenten eines Sende-/Empfangsvorgangs in Millisekunden an.

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

*ResolveTimeout* \[ In\]
</dt> <dd>

Beim Auflösen eines Hostnamens (z.B. `www.microsoft.com` ) in eine IP-Adresse (z.B. 192.168.131.199) in Millisekunden angewendeter Time out-Wert. Der Standardwert ist 0 (null), d. h. kein Time out (unendlich). Wenn das DNS-Timeout mitHILFE von NAME RESOLUTION TIMEOUT angegeben \_ \_ wird, entsteht ein Mehraufwand von einem Thread pro Anforderung.

</dd> <dt>

*ConnectTimeout* \[ In\]
</dt> <dd>

Beim Einrichten eines Kommunikationssockets mit dem Zielserver in Millisekunden wird ein Time out-Wert angewendet. Der Standardwert ist 60.000 (60 Sekunden).

</dd> <dt>

*SendTimeout* \[ In\]
</dt> <dd>

Der Time out-Wert, der beim Senden eines einzelnen Pakets von Anforderungsdaten auf dem Kommunikationssocket an den Zielserver in Millisekunden angewendet wird. Eine große Anforderung, die an einen HTTP-Server gesendet wird, wird normalerweise in mehrere Pakete aufgeteilt. das Sendetime out gilt für das individuelle Senden jedes Pakets. Der Standardwert ist 30.000 (30 Sekunden).

</dd> <dt>

*ReceiveTimeout* \[ In\]
</dt> <dd>

Beim Empfangen eines Pakets mit Antwortdaten vom Zielserver angewendeter Time out-Wert in Millisekunden. Große Antworten werden in mehrere Pakete unterteilt. das Empfangstime out gilt für das Abrufen jedes Datenpakets aus dem Socket. Der Standardwert ist 30.000 (30 Sekunden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK,** andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Alle Parameter sind erforderlich. Mit dem Wert 0 oder -1 wird ein Time out festgelegt, um unendlich zu warten. Ein Wert größer als 0 legt den Time out-Wert in Millisekunden fest. Beispielsweise würde 30.000 das Time out auf 30 Sekunden festlegen. Alle negativen Werte außer -1 führen dazu, dass diese Methode fehlschlägt.

Time out-Werte werden auf der Winsock-Ebene angewendet.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHttp-Startseite.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie alle WinHTTP-Time outs auf 30 Sekunden festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.


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



Das folgende Skriptbeispiel zeigt, wie Sie alle WinHTTP-Time outs auf 30 Sekunden festlegen, eine HTTP-Verbindung öffnen und eine HTTP-Anforderung senden.


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

 

 




