---
description: Legt Anmelde Informationen fest, die mit einem HTTP-Server verwendet werden sollen, egal ob es sich um einen Proxy Server oder einen ursprünglichen Server handelt.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: 'Iwinhttprequest:: Set-Anmelde Informationen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349916"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="4a446-103">Iwinhttprequest:: Set-Anmelde Informationen-Methode</span><span class="sxs-lookup"><span data-stu-id="4a446-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="4a446-104">Die  Methode setanmeldeinformationen legt die Anmelde Informationen für die Verwendung mit einem HTTP-Server fest, egal ob es sich um einen Proxy Server oder einen ursprünglichen Server handelt.</span><span class="sxs-lookup"><span data-stu-id="4a446-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a446-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a446-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="4a446-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a446-107">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a446-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a446-108">Gibt den Benutzernamen für die Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="4a446-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="4a446-109">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a446-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a446-110">Gibt das Kennwort für die Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="4a446-110">Specifies the password for authentication.</span></span> <span data-ttu-id="4a446-111">Dieser Parameter wird ignoriert, wenn *bstrUsername* **null** ist oder fehlt.</span><span class="sxs-lookup"><span data-stu-id="4a446-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="4a446-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4a446-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a446-113">Gibt an, wann [**iwinhttprequest**](iwinhttprequest-interface.md) Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a446-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="4a446-114">Kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4a446-114">Can be one of the following values.</span></span>



| <span data-ttu-id="4a446-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4a446-115">Value</span></span>                                                                                                               | <span data-ttu-id="4a446-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4a446-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4a446-117"><dt>HttpRequest \_ setanmelde Informationen \_ für \_ Server</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="4a446-118">Anmelde Informationen werden an einen Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4a446-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="4a446-119"><dt>HttpRequest \_ setanmelde Informationen \_ für \_ Proxy</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="4a446-120">Anmelde Informationen werden an einen Proxy übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4a446-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a446-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a446-121">Return value</span></span>

<span data-ttu-id="4a446-122">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="4a446-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a446-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a446-123">Remarks</span></span>

<span data-ttu-id="4a446-124">Diese Methode gibt einen Fehlerwert zurück, wenn ein [**offener**](iwinhttprequest-open.md) aufrufsvorgang nicht erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4a446-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="4a446-125">Es wird davon ausgegangen, dass ein gewisses Maß an Interaktion mit einem Proxy Server oder Ursprungsserver auftreten muss, bevor Benutzer Anmelde Informationen für die Sitzung festlegen können.</span><span class="sxs-lookup"><span data-stu-id="4a446-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="4a446-126">Außerdem können die Anmelde Informationen erst formatiert werden, wenn Benutzer wissen, welche Authentifizierungs Schemas unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4a446-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="4a446-127">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="4a446-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="4a446-128">Zum Authentifizieren des Servers und des Proxys muss die Anwendung **setanmelde** Informationen zweimal aufrufen. zuerst, wenn der *Flags* -Parameter auf **HttpRequest \_ setanmelde Informationen \_ für \_ Server** und Second festgelegt ist und der *Flags* -Parameter auf **HttpRequest \_ setanmelde Informationen \_ für \_ Proxy** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4a446-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="4a446-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a446-129">Examples</span></span>

<span data-ttu-id="4a446-130">Das folgende Beispiel zeigt, wie Sie eine HTTP-Verbindung öffnen, Anmelde Informationen für den Server festlegen, eine HTTP-Anforderung senden und den Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="4a446-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="4a446-131">Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4a446-131">This example must be run from a command prompt.</span></span>


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
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="4a446-132">Im folgenden Beispielskript wird veranschaulicht, wie eine HTTP-Verbindung geöffnet, Anmelde Informationen für den Server festgelegt, Anmelde Informationen für einen Proxy festgelegt werden, wenn ein Proxy verwendet wird, eine HTTP-Anforderung gesendet und der Antworttext gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="4a446-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="4a446-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a446-133">Requirements</span></span>



| <span data-ttu-id="4a446-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a446-134">Requirement</span></span> | <span data-ttu-id="4a446-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4a446-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a446-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a446-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4a446-137">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a446-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4a446-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a446-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4a446-139">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a446-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4a446-140">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4a446-140">Redistributable</span></span><br/>          | <span data-ttu-id="4a446-141">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4a446-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4a446-142">IDL</span><span class="sxs-lookup"><span data-stu-id="4a446-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a446-143"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4a446-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a446-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a446-145"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4a446-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4a446-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a446-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4a446-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a446-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a446-149">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="4a446-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4a446-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4a446-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4a446-151">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="4a446-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




