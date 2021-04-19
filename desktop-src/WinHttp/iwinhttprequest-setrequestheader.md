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
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="2e606-103">Iwinhttprequest:: ltrequestheader-Methode</span><span class="sxs-lookup"><span data-stu-id="2e606-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="2e606-104">Mit der Methode " **ltrequestheader** " wird ein HTTP-Anforderungs Header hinzugefügt, geändert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2e606-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e606-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e606-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="2e606-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e606-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e606-107">*Header* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e606-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e606-108">Gibt den Namen des festzulegenden Headers an, z. b. "Tiefe".</span><span class="sxs-lookup"><span data-stu-id="2e606-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="2e606-109">Dieser Parameter darf keinen Doppelpunkt enthalten und muss den eigentlichen Text des HTTP-Headers enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e606-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="2e606-110">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e606-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e606-111">Gibt den Wert des Headers an, z. b. "unendlich".</span><span class="sxs-lookup"><span data-stu-id="2e606-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e606-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e606-112">Return value</span></span>

<span data-ttu-id="2e606-113">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="2e606-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e606-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e606-114">Remarks</span></span>

<span data-ttu-id="2e606-115">Header werden über Umleitungen übertragen.</span><span class="sxs-lookup"><span data-stu-id="2e606-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="2e606-116">Dies kann zu einem Sicherheitsrisiko führen.</span><span class="sxs-lookup"><span data-stu-id="2e606-116">This can create a security vulnerability.</span></span> <span data-ttu-id="2e606-117">Um zu vermeiden, dass Header bei einer Umleitung übertragen werden, korrigieren Sie mithilfe des [*WinHTTP- \_ Status \_ Rückruf*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) Rückrufs die spezifischen Header, wenn eine Umleitung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2e606-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="2e606-118">Mit der **setrequestheader** -Methode kann die aufrufende Anwendung einen HTTP-Anforderungs Header vor dem Senden der Anforderung hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="2e606-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="2e606-119">Der Header Name wird in der *Kopfzeile* angegeben, und das Header Token oder der Wert wird als *Wert* angegeben.</span><span class="sxs-lookup"><span data-stu-id="2e606-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="2e606-120">Um einen Header hinzuzufügen, geben Sie einen Header Namen und einen Wert an.</span><span class="sxs-lookup"><span data-stu-id="2e606-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="2e606-121">Wenn eine andere Kopfzeile mit diesem Namen bereits vorhanden ist, wird Sie ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2e606-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="2e606-122">Zum Löschen eines Headers legen Sie den *Header* auf den Namen des zu löschenden Headers fest, und legen Sie den *Wert* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="2e606-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="2e606-123">Der Name und der Wert der Anforderungs Header, die mit dieser Methode hinzugefügt werden, werden überprüft.</span><span class="sxs-lookup"><span data-stu-id="2e606-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="2e606-124">Header müssen wohl geformt sein.</span><span class="sxs-lookup"><span data-stu-id="2e606-124">Headers must be well formed.</span></span> <span data-ttu-id="2e606-125">Weitere Informationen zu gültigen HTTP-Headern finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="2e606-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="2e606-126">Wenn ein ungültiger Header verwendet wird, tritt ein Fehler auf, und der Header wird nicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2e606-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="2e606-127">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="2e606-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2e606-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e606-128">Examples</span></span>

<span data-ttu-id="2e606-129">Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, einen Anforderungs Header festlegen, eine HTTP-Anforderung senden und den Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="2e606-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="2e606-130">Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2e606-130">This example must be run from a command prompt.</span></span>


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



<span data-ttu-id="2e606-131">Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, ein Anforderungs Header festgelegt und eine HTTP-Anforderung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e606-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2e606-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e606-132">Requirements</span></span>



| <span data-ttu-id="2e606-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e606-133">Requirement</span></span> | <span data-ttu-id="2e606-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2e606-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e606-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e606-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2e606-136">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e606-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2e606-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e606-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2e606-138">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e606-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2e606-139">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2e606-139">Redistributable</span></span><br/>          | <span data-ttu-id="2e606-140">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2e606-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2e606-141">IDL</span><span class="sxs-lookup"><span data-stu-id="2e606-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e606-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e606-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e606-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e606-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e606-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e606-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="2e606-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2e606-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e606-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e606-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2e606-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e606-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e606-148">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="2e606-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="2e606-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2e606-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2e606-150">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="2e606-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

