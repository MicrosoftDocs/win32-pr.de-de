---
description: Ruft alle HTTP-Antwortheader ab.
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: 'Iwinhttprequest:: getallresponsheaders-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355341"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="247b2-103">Iwinhttprequest:: getallresponsheaders-Methode</span><span class="sxs-lookup"><span data-stu-id="247b2-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="247b2-104">Die **getallresponsheaders** -Methode ruft alle HTTP-Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="247b2-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="247b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="247b2-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="247b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="247b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="247b2-107">*Header* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="247b2-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="247b2-108">Empfängt die resultierenden Header Informationen.</span><span class="sxs-lookup"><span data-stu-id="247b2-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="247b2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="247b2-109">Return value</span></span>

<span data-ttu-id="247b2-110">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="247b2-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="247b2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="247b2-111">Remarks</span></span>

<span data-ttu-id="247b2-112">Diese Methode gibt alle Header zurück, die in der letzten Serverantwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="247b2-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="247b2-113">Die einzelnen Header werden durch eine Kombination aus Wagen Rücklauf und Zeilenvorschub (ASCII 13 und 10) getrennt.</span><span class="sxs-lookup"><span data-stu-id="247b2-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="247b2-114">Auf den letzten Eintrag folgen zwei Trennzeichen (13, 10, 13, 10).</span><span class="sxs-lookup"><span data-stu-id="247b2-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="247b2-115">Rufen Sie diese Methode nur auf, nachdem die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="247b2-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="247b2-116">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="247b2-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="247b2-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="247b2-117">Examples</span></span>

<span data-ttu-id="247b2-118">Im folgenden Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und alle Header aus der Antwort erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="247b2-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="247b2-119">Dieses Beispiel sollte über eine Eingabeaufforderung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="247b2-119">This example should be run from a command prompt.</span></span>


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    // Variable for return value
    HRESULT    hr;

    // Initialize COM
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



<span data-ttu-id="247b2-120">Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und alle Header aus der Antwort erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="247b2-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="247b2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="247b2-121">Requirements</span></span>



| <span data-ttu-id="247b2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="247b2-122">Requirement</span></span> | <span data-ttu-id="247b2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="247b2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="247b2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="247b2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="247b2-125">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="247b2-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="247b2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="247b2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="247b2-127">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="247b2-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="247b2-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="247b2-128">Redistributable</span></span><br/>          | <span data-ttu-id="247b2-129">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="247b2-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="247b2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="247b2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="247b2-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="247b2-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="247b2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="247b2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="247b2-133"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="247b2-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="247b2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="247b2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="247b2-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="247b2-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="247b2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="247b2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247b2-137">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="247b2-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="247b2-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="247b2-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="247b2-139">**Getresponsheader**</span><span class="sxs-lookup"><span data-stu-id="247b2-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="247b2-140">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="247b2-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




