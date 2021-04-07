---
description: Die Send-Methode sendet eine HTTP-Anforderung an einen HTTP-Server.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: 'Iwinhttprequest:: Send-Methode'
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
ms.openlocfilehash: 0040ed6c09814a2b2112a91173d84430b8130a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758329"
---
# <a name="iwinhttprequestsend-method"></a><span data-ttu-id="138db-103">Iwinhttprequest:: Send-Methode</span><span class="sxs-lookup"><span data-stu-id="138db-103">IWinHttpRequest::Send method</span></span>

<span data-ttu-id="138db-104">Die **Send** -Methode sendet eine HTTP-Anforderung an einen HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="138db-104">The **Send** method sends an HTTP request to an HTTP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="138db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="138db-105">Syntax</span></span>


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a><span data-ttu-id="138db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="138db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="138db-107">*Textkörper* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="138db-107">*Body* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="138db-108">Die an den Server zu sendenden Daten.</span><span class="sxs-lookup"><span data-stu-id="138db-108">Data to be sent to the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="138db-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="138db-109">Return value</span></span>

<span data-ttu-id="138db-110">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="138db-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="138db-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="138db-111">Remarks</span></span>

<span data-ttu-id="138db-112">Die Anforderung, die gesendet werden soll, wurde in einem vorherigen Aufrufder [**Open**](iwinhttprequest-open.md) -Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="138db-112">The request to be sent was defined in a prior call to the [**Open**](iwinhttprequest-open.md) method.</span></span> <span data-ttu-id="138db-113">Die aufrufende Anwendung kann Daten bereitstellen, die über den *Body* -Parameter an den Server gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="138db-113">The calling application can provide data to be sent to the server through the *Body* parameter.</span></span> <span data-ttu-id="138db-114">Wenn das [*http-Verb*](glossary.md) des [**geöffneten**](iwinhttprequest-open.md) Objekts "Get" ist, sendet diese Methode die Anforderung ohne *Text*, auch wenn Sie von der aufrufenden Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="138db-114">If the [*HTTP verb*](glossary.md) of the object's [**Open**](iwinhttprequest-open.md) is "GET", this method sends the request without *Body*, even if it is provided by the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="138db-115">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="138db-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="138db-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="138db-116">Examples</span></span>

<span data-ttu-id="138db-117">Im folgenden Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="138db-117">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="138db-118">Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="138db-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="138db-119">Im folgenden Skript Beispiel wird gezeigt, wie Sie Daten auf einem HTTP-Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="138db-119">The following scripting example shows how to post data to an HTTP server.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a><span data-ttu-id="138db-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="138db-120">Requirements</span></span>



| <span data-ttu-id="138db-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="138db-121">Requirement</span></span> | <span data-ttu-id="138db-122">Wert</span><span class="sxs-lookup"><span data-stu-id="138db-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="138db-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="138db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="138db-124">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="138db-124">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="138db-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="138db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="138db-126">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="138db-126">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="138db-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="138db-127">Redistributable</span></span><br/>          | <span data-ttu-id="138db-128">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="138db-128">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="138db-129">IDL</span><span class="sxs-lookup"><span data-stu-id="138db-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="138db-130"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="138db-130"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="138db-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="138db-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="138db-132"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="138db-132"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="138db-133">DLL</span><span class="sxs-lookup"><span data-stu-id="138db-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="138db-134"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="138db-134"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="138db-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="138db-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138db-136">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="138db-136">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="138db-137">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="138db-137">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="138db-138">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="138db-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




