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
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="9ff97-103">Iwinhttprequest:: WaitForResponse-Methode</span><span class="sxs-lookup"><span data-stu-id="9ff97-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="9ff97-104">Die **WaitForResponse** -Methode wartet auf den Abschluss einer asynchronen [**Sende**](iwinhttprequest-send.md) Methode mit optionalem Timeout Wert (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9ff97-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff97-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ff97-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="9ff97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ff97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff97-107">*Timeout* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9ff97-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff97-108">Timeout Wert in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9ff97-108">Time-out value, in seconds.</span></span> <span data-ttu-id="9ff97-109">Das Standard Timeout ist unendlich.</span><span class="sxs-lookup"><span data-stu-id="9ff97-109">Default time-out is infinite.</span></span> <span data-ttu-id="9ff97-110">Wenn Sie das Timeout explizit auf unendlich festlegen möchten, verwenden Sie den Wert-1.</span><span class="sxs-lookup"><span data-stu-id="9ff97-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="9ff97-111">*Erfolgreich* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9ff97-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff97-112">Empfängt einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="9ff97-112">Receives one of the following values.</span></span>



| <span data-ttu-id="9ff97-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9ff97-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="9ff97-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9ff97-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="9ff97-115"><dt>**Variant \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff97-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="9ff97-116">Eine Antwort wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="9ff97-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="9ff97-117"><dt>**Variant \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff97-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9ff97-118">Der angegebene Timeout Zeitraum wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="9ff97-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff97-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ff97-119">Return value</span></span>

<span data-ttu-id="9ff97-120">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="9ff97-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff97-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ff97-121">Remarks</span></span>

<span data-ttu-id="9ff97-122">Diese Methode hält die Ausführung an und wartet auf eine Antwort auf eine asynchrone Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9ff97-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="9ff97-123">Diese Methode sollte nach einem [**Send**](iwinhttprequest-send.md)-Vorgang aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9ff97-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="9ff97-124">Beim Aufrufen von Anwendungen kann ein optionaler *Timeout* Wert (in Sekunden) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ff97-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="9ff97-125">Wenn für diese Methode ein Timeout auftritt, wird die Anforderung nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9ff97-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="9ff97-126">Auf diese Weise kann die aufrufende Anwendung in einem nachfolgenden Aufruf dieser Methode weiterhin auf die Anforderung warten.</span><span class="sxs-lookup"><span data-stu-id="9ff97-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="9ff97-127">Das Aufrufen dieser Eigenschaft nach einer synchronen [**Send**](iwinhttprequest-send.md) -Methode wird sofort zurückgegeben und hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="9ff97-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="9ff97-128">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="9ff97-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9ff97-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ff97-129">Examples</span></span>

<span data-ttu-id="9ff97-130">Das folgende Beispiel zeigt, wie Sie eine asynchrone HTTP-Verbindung öffnen, eine HTTP-Anforderung senden, auf die Antwort warten und den Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="9ff97-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


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



<span data-ttu-id="9ff97-131">Im folgenden Skript Beispiel wird gezeigt, wie eine asynchrone HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet, auf eine Antwort gewartet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="9ff97-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9ff97-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ff97-132">Requirements</span></span>



| <span data-ttu-id="9ff97-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ff97-133">Requirement</span></span> | <span data-ttu-id="9ff97-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9ff97-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff97-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ff97-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff97-136">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ff97-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="9ff97-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ff97-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff97-138">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ff97-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="9ff97-139">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9ff97-139">Redistributable</span></span><br/>          | <span data-ttu-id="9ff97-140">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9ff97-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="9ff97-141">IDL</span><span class="sxs-lookup"><span data-stu-id="9ff97-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ff97-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ff97-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="9ff97-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ff97-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ff97-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ff97-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="9ff97-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff97-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff97-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff97-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9ff97-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ff97-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff97-148">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="9ff97-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="9ff97-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="9ff97-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="9ff97-150">**Eren**</span><span class="sxs-lookup"><span data-stu-id="9ff97-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="9ff97-151">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="9ff97-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




