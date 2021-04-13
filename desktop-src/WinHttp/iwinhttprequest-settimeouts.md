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
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="b8d0d-103">Iwinhttprequest:: settimeouts-Methode</span><span class="sxs-lookup"><span data-stu-id="b8d0d-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="b8d0d-104">Die **settimeouts** -Methode gibt die einzelnen Timeout Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8d0d-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="b8d0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8d0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d0d-107">*Resolvetimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d0d-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d0d-108">Timeout Wert, der beim Auflösen eines Host namens (z. b. `www.microsoft.com` ) in eine IP-Adresse (z. b. 192.168.131.199) in Millisekunden angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="b8d0d-109">Der Standardwert ist 0 (null), was bedeutet, dass kein Timeout (unendlich) auftritt.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="b8d0d-110">Wenn das DNS-Timeout mithilfe \_ des Namens Auflösungs \_ Timeouts angegeben wird, entsteht ein mehr Aufwand von einem Thread pro Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="b8d0d-111">*ConnectTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d0d-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d0d-112">Timeout Wert, der beim Einrichten eines Kommunikations Sockets mit dem Zielserver (in Millisekunden) angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="b8d0d-113">Der Standardwert ist 60.000 (60 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="b8d0d-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="b8d0d-114">*SendTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d0d-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d0d-115">Timeout Wert, der beim Senden eines einzelnen Pakets mit Anforderungs Daten auf dem Kommunikations Socket an den Zielserver (in Millisekunden) angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="b8d0d-116">Eine große Anforderung, die an einen HTTP-Server gesendet wird, wird normalerweise in mehrere Pakete aufgeteilt. das Sende Timeout gilt für das einzelne Senden der einzelnen Pakete.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="b8d0d-117">Der Standardwert ist 30.000 (30 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="b8d0d-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="b8d0d-118">*ReceiveTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d0d-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d0d-119">Timeout Wert, der beim Empfangen eines Pakets mit Antwortdaten vom Zielserver in Millisekunden angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="b8d0d-120">Große Antworten werden in mehrere Pakete aufgeteilt. der Empfangs Timeout bezieht sich auf das Abrufen der einzelnen Datenpakete vom Socket.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="b8d0d-121">Der Standardwert ist 30.000 (30 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="b8d0d-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d0d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8d0d-122">Return value</span></span>

<span data-ttu-id="b8d0d-123">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d0d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8d0d-124">Remarks</span></span>

<span data-ttu-id="b8d0d-125">Alle Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-125">All parameters are required.</span></span> <span data-ttu-id="b8d0d-126">Mit dem Wert 0 oder-1 wird ein Timeout festgelegt, um unendlich zu warten.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="b8d0d-127">Ein Wert größer 0 (null) legt den Timeout Wert in Millisekunden fest.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="b8d0d-128">Beispielsweise würde 30.000 das Timeout auf 30 Sekunden festlegen.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="b8d0d-129">Alle negativen Werte, mit Ausnahme von-1, führen dazu, dass diese Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="b8d0d-130">Timeout Werte werden auf der Winsock-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="b8d0d-131">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b8d0d-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8d0d-132">Examples</span></span>

<span data-ttu-id="b8d0d-133">Das folgende Beispiel zeigt, wie Sie alle WinHTTP-Timeouts auf 30 Sekunden festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="b8d0d-134">Im folgenden Skript Beispiel wird gezeigt, wie alle WinHTTP-Timeouts auf 30 Sekunden festgelegt werden, eine HTTP-Verbindung geöffnet und eine HTTP-Anforderung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b8d0d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8d0d-135">Requirements</span></span>



| <span data-ttu-id="b8d0d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8d0d-136">Requirement</span></span> | <span data-ttu-id="b8d0d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b8d0d-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d0d-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8d0d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d0d-139">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8d0d-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b8d0d-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8d0d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d0d-141">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8d0d-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b8d0d-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b8d0d-142">Redistributable</span></span><br/>          | <span data-ttu-id="b8d0d-143">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b8d0d-144">IDL</span><span class="sxs-lookup"><span data-stu-id="b8d0d-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8d0d-145"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8d0d-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="b8d0d-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8d0d-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8d0d-147"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8d0d-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="b8d0d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b8d0d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8d0d-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d0d-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8d0d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8d0d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d0d-151">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="b8d0d-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="b8d0d-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b8d0d-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="b8d0d-153">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="b8d0d-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




