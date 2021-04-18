---
description: Ruft den Text der Antwort Entität als Text ab.
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: 'Iwinhttprequest:: Response Text-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351418"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="11a73-103">Iwinhttprequest:: Response Text-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="11a73-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="11a73-104">Die Response **Text** -Eigenschaft ruft den Text der Antwort Entität als Text ab.</span><span class="sxs-lookup"><span data-stu-id="11a73-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="11a73-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="11a73-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a73-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a73-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="11a73-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="11a73-107">Property value</span></span>

<span data-ttu-id="11a73-108">**BSTR** , das den Entitäts Text der Antwort als Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="11a73-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11a73-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="11a73-109">Error codes</span></span>

<span data-ttu-id="11a73-110">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="11a73-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a73-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11a73-111">Remarks</span></span>

<span data-ttu-id="11a73-112">Diese Eigenschaft kann nur aufgerufen werden, nachdem die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="11a73-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="11a73-113">Wenn Sie diese Eigenschaft im synchronen Modus verwenden, beträgt der Grenzwert für die Anzahl der zurückgegebenen Zeichen ungefähr 2.169.895.</span><span class="sxs-lookup"><span data-stu-id="11a73-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="11a73-114">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="11a73-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="11a73-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11a73-115">Examples</span></span>

<span data-ttu-id="11a73-116">Im folgenden Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="11a73-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="11a73-117">Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="11a73-117">This example must be run from a command prompt.</span></span>


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
    {   // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print the response to a console.
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



<span data-ttu-id="11a73-118">Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="11a73-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="11a73-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11a73-119">Requirements</span></span>



| <span data-ttu-id="11a73-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11a73-120">Requirement</span></span> | <span data-ttu-id="11a73-121">Wert</span><span class="sxs-lookup"><span data-stu-id="11a73-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a73-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11a73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="11a73-123">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11a73-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="11a73-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11a73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="11a73-125">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11a73-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="11a73-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="11a73-126">Redistributable</span></span><br/>          | <span data-ttu-id="11a73-127">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="11a73-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="11a73-128">IDL</span><span class="sxs-lookup"><span data-stu-id="11a73-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11a73-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="11a73-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11a73-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="11a73-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="11a73-132">DLL</span><span class="sxs-lookup"><span data-stu-id="11a73-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11a73-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="11a73-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11a73-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a73-135">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="11a73-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="11a73-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="11a73-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="11a73-137">**Response Body**</span><span class="sxs-lookup"><span data-stu-id="11a73-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="11a73-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="11a73-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="11a73-139">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="11a73-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




