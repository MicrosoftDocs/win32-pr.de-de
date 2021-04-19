---
description: Legt Proxy Server Informationen fest.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'Iwinhttprequest:: SetProxy-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352602"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="ecf04-103">Iwinhttprequest:: SetProxy-Methode</span><span class="sxs-lookup"><span data-stu-id="ecf04-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="ecf04-104">Die **SetProxy** -Methode legt Proxy Server Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="ecf04-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf04-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecf04-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="ecf04-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecf04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf04-107">*Proxysetting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf04-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf04-108">Die Flags, die diese Methode steuern.</span><span class="sxs-lookup"><span data-stu-id="ecf04-108">The flags that control this method.</span></span> <span data-ttu-id="ecf04-109">Kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ecf04-109">Can be one of the following values.</span></span>



| <span data-ttu-id="ecf04-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ecf04-110">Value</span></span>                                                                                                           | <span data-ttu-id="ecf04-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ecf04-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ecf04-112"><dt>HttpRequest \_ proxysetting \_ Standard</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="ecf04-113">Standard Proxy Einstellung.</span><span class="sxs-lookup"><span data-stu-id="ecf04-113">Default proxy setting.</span></span> <span data-ttu-id="ecf04-114">Äquivalent zu **HttpRequest \_ proxysetting \_ preconfig**.</span><span class="sxs-lookup"><span data-stu-id="ecf04-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="ecf04-115"><dt>HttpRequest \_ proxysetting \_ preconfig</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="ecf04-116">Gibt an, dass die Proxy Einstellungen aus der Registrierung abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ecf04-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="ecf04-117">Dabei wird davon ausgegangen, dass [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ecf04-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="ecf04-118">Wenn Proxycfg.exe nicht ausgeführt wurde und **HttpRequest \_ proxysetting \_ preconfig** angegeben ist, entspricht das Verhalten dem **HttpRequest \_ proxysetting \_ Direct**.</span><span class="sxs-lookup"><span data-stu-id="ecf04-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="ecf04-119"><dt>HttpRequest \_ proxysetting \_ Direct</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="ecf04-120">Gibt an, dass direkt auf alle HTTP-und HTTPS-Server zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf04-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="ecf04-121">Verwenden Sie diesen Befehl, wenn kein Proxy Server vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ecf04-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ecf04-122"><dt>HttpRequest \_ proxysetting- \_ Proxy</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="ecf04-123">Wenn **HttpRequest \_ proxysetting \_ Proxy** angegeben ist, muss *varproxyserver* auf eine Proxy Server Zeichenfolge festgelegt werden, und *varbypasslist* sollte auf eine Domänen Umgehungs Listen-Zeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ecf04-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="ecf04-124">Diese Proxykonfiguration gilt nur für die aktuelle Instanz des [**WinHttpRequest**](winhttprequest.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ecf04-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="ecf04-125">*Proxy Server* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ecf04-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf04-126">Legen Sie auf eine Proxy Server Zeichenfolge fest, wenn *proxysetting* dem **HttpRequest \_ proxysetting- \_ Proxy** entspricht.</span><span class="sxs-lookup"><span data-stu-id="ecf04-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="ecf04-127">*BypassList* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ecf04-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf04-128">Festlegen auf eine Domänen Umgehungs Listen-Zeichenfolge, wenn *proxysetting* dem **HttpRequest \_ proxysetting- \_ Proxy** entspricht.</span><span class="sxs-lookup"><span data-stu-id="ecf04-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf04-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecf04-129">Return value</span></span>

<span data-ttu-id="ecf04-130">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="ecf04-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf04-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecf04-131">Remarks</span></span>

<span data-ttu-id="ecf04-132">Ermöglicht es der aufrufenden Anwendung, die Verwendung von Standard Proxy Informationen (konfiguriert durch das Proxy Konfigurationstool) oder das Überschreiben von [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md)anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ecf04-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="ecf04-133">Diese Methode muss aufgerufen werden, bevor die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ecf04-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="ecf04-134">Wenn diese Methode nach der [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wird, hat Sie keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="ecf04-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="ecf04-135">[**Iwinhttprequest**](iwinhttprequest-interface.md) übergibt diese Parameter an Microsoft Windows HTTP-Dienste (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="ecf04-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="ecf04-136">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="ecf04-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ecf04-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecf04-137">Examples</span></span>

<span data-ttu-id="ecf04-138">Das folgende Beispiel zeigt, wie Sie die Proxy Einstellungen für einen bestimmten Proxy Server festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="ecf04-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="ecf04-139">Dieses Beispiel muss von einer Eingabeaufforderung aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ecf04-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="ecf04-140">Diese Proxy Einstellungen funktionieren nur, wenn Sie über einen Proxy Server mit dem Namen "Proxy \_ Server" verfügen, der Port 80 verwendet, und der Computer den Proxy Server umgehen kann, wenn der Hostname auf ". Microsoft.com" endet.</span><span class="sxs-lookup"><span data-stu-id="ecf04-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


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
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
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
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="ecf04-141">Das folgende Beispielskript zeigt, wie Sie die Proxy Einstellungen für einen bestimmten Proxy Server festlegen, eine HTTP-Verbindung öffnen, eine HTTP-Anforderung senden und den Antworttext lesen.</span><span class="sxs-lookup"><span data-stu-id="ecf04-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="ecf04-142">Diese Proxy Einstellungen funktionieren nur, wenn Sie über einen Proxy Server mit dem Namen "Proxy \_ Server" verfügen, der Port 80 verwendet, und der Computer den Proxy Server umgehen kann, wenn der Hostname auf ". Microsoft.com" endet.</span><span class="sxs-lookup"><span data-stu-id="ecf04-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="ecf04-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecf04-143">Requirements</span></span>



| <span data-ttu-id="ecf04-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecf04-144">Requirement</span></span> | <span data-ttu-id="ecf04-145">Wert</span><span class="sxs-lookup"><span data-stu-id="ecf04-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf04-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecf04-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf04-147">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecf04-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ecf04-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecf04-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf04-149">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecf04-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="ecf04-150">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ecf04-150">Redistributable</span></span><br/>          | <span data-ttu-id="ecf04-151">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ecf04-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="ecf04-152">IDL</span><span class="sxs-lookup"><span data-stu-id="ecf04-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ecf04-153"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="ecf04-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ecf04-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecf04-155"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ecf04-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ecf04-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecf04-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf04-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ecf04-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecf04-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf04-159">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="ecf04-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="ecf04-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ecf04-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="ecf04-161">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="ecf04-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




