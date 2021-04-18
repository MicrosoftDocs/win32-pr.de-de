---
description: Ruft die HTTP-Antwortheader ab.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: 'Iwinhttprequest:: getresponsheader-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351033"
---
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="2f16a-103">Iwinhttprequest:: getresponsheader-Methode</span><span class="sxs-lookup"><span data-stu-id="2f16a-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="2f16a-104">Die **getresponsheader** -Methode ruft die HTTP-Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="2f16a-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f16a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f16a-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="2f16a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f16a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f16a-107">*Header* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f16a-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f16a-108">Gibt den Header Namen der Groß-/Kleinschreibung an.</span><span class="sxs-lookup"><span data-stu-id="2f16a-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="2f16a-109">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f16a-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2f16a-110">Empfängt die resultierenden Header Informationen.</span><span class="sxs-lookup"><span data-stu-id="2f16a-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f16a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f16a-111">Return value</span></span>

<span data-ttu-id="2f16a-112">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="2f16a-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f16a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f16a-113">Remarks</span></span>

<span data-ttu-id="2f16a-114">Diese Methode gibt den Wert des Antwort Headers namens in- *Header* zurück.</span><span class="sxs-lookup"><span data-stu-id="2f16a-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="2f16a-115">Beachten Sie, dass Automatisierungs Clients, wie z. b. Skripts, die Header Daten als Rückgabewert des Funktions Aufrufes abrufen, nicht über einen Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="2f16a-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="2f16a-116">Rufen Sie diese Methode nur auf, nachdem die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2f16a-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="2f16a-117">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="2f16a-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2f16a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f16a-118">Examples</span></span>

<span data-ttu-id="2f16a-119">Im folgenden Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Datums Header aus der Antwort erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="2f16a-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="2f16a-120">Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2f16a-120">This example must be run from a command prompt.</span></span>


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

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                         &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
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



<span data-ttu-id="2f16a-121">Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Datums Header aus der Antwort erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="2f16a-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
```



## <a name="requirements"></a><span data-ttu-id="2f16a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f16a-122">Requirements</span></span>



| <span data-ttu-id="2f16a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f16a-123">Requirement</span></span> | <span data-ttu-id="2f16a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2f16a-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f16a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f16a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2f16a-126">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f16a-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2f16a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f16a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2f16a-128">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f16a-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2f16a-129">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2f16a-129">Redistributable</span></span><br/>          | <span data-ttu-id="2f16a-130">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2f16a-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2f16a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="2f16a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f16a-132"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f16a-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="2f16a-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f16a-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f16a-134"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f16a-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="2f16a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2f16a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f16a-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f16a-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f16a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f16a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f16a-138">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="2f16a-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="2f16a-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2f16a-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2f16a-140">**Getallresponcheaders**</span><span class="sxs-lookup"><span data-stu-id="2f16a-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="2f16a-141">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="2f16a-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




