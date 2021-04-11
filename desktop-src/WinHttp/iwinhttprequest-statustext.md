---
description: Ruft den HTTP-Status Text ab.
ms.assetid: 480babbd-432c-4722-98df-a73ba5928e1f
title: 'Iwinhttprequest:: statusText-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.StatusText
- IWinHttpRequest.get_StatusText
- WinHttpRequest.StatusText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 41288d87b8194caf3a2a14cc89cd5acbffec902c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050595"
---
# <a name="iwinhttprequeststatustext-property"></a><span data-ttu-id="a5f14-103">Iwinhttprequest:: statusText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a5f14-103">IWinHttpRequest::StatusText property</span></span>

<span data-ttu-id="a5f14-104">Die **Statustext** -Eigenschaft ruft den HTTP-Status Text ab.</span><span class="sxs-lookup"><span data-stu-id="a5f14-104">The **StatusText** property retrieves the HTTP status text.</span></span>

<span data-ttu-id="a5f14-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a5f14-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f14-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5f14-106">Syntax</span></span>


```C++
HRESULT get_StatusText(
  [out, retval] BSTR *Status
);
```


```JScript

StatusText = WinHttpRequest.StatusText
```





## <a name="property-value"></a><span data-ttu-id="a5f14-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a5f14-107">Property value</span></span>

<span data-ttu-id="a5f14-108">**BSTR** , das den HTTP-Status Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="a5f14-108">**BSTR** that receives the HTTP status text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5f14-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a5f14-109">Error codes</span></span>

<span data-ttu-id="a5f14-110">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="a5f14-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f14-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5f14-111">Remarks</span></span>

<span data-ttu-id="a5f14-112">Ruft den Textteil der Serverantwort Zeile ab und stellt die "benutzerfreundliche"-Entsprechung für den numerischen HTTP-Statuscode bereit.</span><span class="sxs-lookup"><span data-stu-id="a5f14-112">Retrieves the text portion of the server response line, making available the "user-friendly" equivalent to the numeric HTTP status code.</span></span> <span data-ttu-id="a5f14-113">Die Ergebnisse dieser Eigenschaft sind nur gültig, nachdem die [**Send**](iwinhttprequest-send.md) -Methode erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f14-113">The results of this property are valid only after the [**Send**](iwinhttprequest-send.md) method has successfully completed.</span></span>

> [!Note]  
> <span data-ttu-id="a5f14-114">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="a5f14-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a5f14-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5f14-115">Examples</span></span>

<span data-ttu-id="a5f14-116">Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden, den [**Status**](iwinhttprequest-status.md) und den Status **anzeigen und den** Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="a5f14-116">The following example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response text.</span></span> <span data-ttu-id="a5f14-117">Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a5f14-117">This example must be run from a command prompt.</span></span>


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
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

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
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="a5f14-118">Im folgenden Beispielskript wird veranschaulicht, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet, der [**Status**](iwinhttprequest-status.md) und der Status angezeigt und die Antwortheader **gelesen werden.**</span><span class="sxs-lookup"><span data-stu-id="a5f14-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response headers.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="a5f14-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5f14-119">Requirements</span></span>



| <span data-ttu-id="a5f14-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5f14-120">Requirement</span></span> | <span data-ttu-id="a5f14-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a5f14-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f14-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5f14-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f14-123">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5f14-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="a5f14-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5f14-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f14-125">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5f14-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="a5f14-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a5f14-126">Redistributable</span></span><br/>          | <span data-ttu-id="a5f14-127">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a5f14-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="a5f14-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a5f14-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5f14-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5f14-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="a5f14-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5f14-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5f14-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5f14-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="a5f14-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a5f14-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5f14-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5f14-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a5f14-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5f14-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f14-135">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="a5f14-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="a5f14-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a5f14-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="a5f14-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="a5f14-137">**Status**</span></span>](iwinhttprequest-status.md)
</dt> <dt>

[<span data-ttu-id="a5f14-138">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="a5f14-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




