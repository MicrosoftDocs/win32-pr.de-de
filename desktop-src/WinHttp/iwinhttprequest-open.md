---
description: Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: 'Iwinhttprequest:: Open-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358998"
---
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="3f541-103">Iwinhttprequest:: Open-Methode</span><span class="sxs-lookup"><span data-stu-id="3f541-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="3f541-104">Die **Open** -Methode öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="3f541-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f541-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f541-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="3f541-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f541-107">*Methode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f541-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f541-108">Gibt das für die **Open** -Methode verwendete [*http-Verb*](glossary.md) an, z. b. "Get" oder "Put".</span><span class="sxs-lookup"><span data-stu-id="3f541-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="3f541-109">Verwenden Sie immer Großbuchstaben, da einige Server klein geschriebene *http-Verb* s ignorieren.</span><span class="sxs-lookup"><span data-stu-id="3f541-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="3f541-110">*URL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f541-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f541-111">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="3f541-111">Specifies the name of the resource.</span></span> <span data-ttu-id="3f541-112">Dabei muss es sich um einen absolute URL handeln.</span><span class="sxs-lookup"><span data-stu-id="3f541-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="3f541-113">*Async* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3f541-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3f541-114">Gibt an, ob im asynchronen Modus geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f541-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="3f541-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3f541-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="3f541-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3f541-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="3f541-117"><dt>**Variant \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3f541-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3f541-118">Öffnet die HTTP-Verbindung im synchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="3f541-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="3f541-119">Ein [**Sende**](iwinhttprequest-send.md) Vorgang wird nicht zurückgegeben, bis die Antwort von [WinHTTP](about-winhttp.md) vollständig empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="3f541-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="3f541-120"><dt>**Variant \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="3f541-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="3f541-121">Öffnet die HTTP-Verbindung im asynchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="3f541-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f541-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f541-122">Return value</span></span>

<span data-ttu-id="3f541-123">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="3f541-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f541-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f541-124">Remarks</span></span>

<span data-ttu-id="3f541-125">Diese Methode öffnet eine Verbindung mit der in *URL* identifizierten Ressource unter Verwendung des [*HTTP-Verbs*](glossary.md) , das in der- *Methode* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3f541-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="3f541-126">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="3f541-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3f541-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f541-127">Examples</span></span>

<span data-ttu-id="3f541-128">Im folgenden Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="3f541-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
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



<span data-ttu-id="3f541-129">Im folgenden Skript Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="3f541-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3f541-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f541-130">Requirements</span></span>



| <span data-ttu-id="3f541-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f541-131">Requirement</span></span> | <span data-ttu-id="3f541-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3f541-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f541-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f541-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3f541-134">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f541-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="3f541-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f541-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3f541-136">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f541-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="3f541-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3f541-137">Redistributable</span></span><br/>          | <span data-ttu-id="3f541-138">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3f541-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="3f541-139">IDL</span><span class="sxs-lookup"><span data-stu-id="3f541-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f541-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f541-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="3f541-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f541-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f541-142"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f541-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="3f541-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3f541-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f541-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f541-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3f541-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f541-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f541-146">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="3f541-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="3f541-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="3f541-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="3f541-148">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="3f541-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




