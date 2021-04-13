---
title: InternetGetProxyInfo-Funktion
description: Ruft Proxy Daten für den Zugriff auf angegebene Ressourcen ab.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Internetgetproxyinfo-Funktion WinInet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391927"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="72338-104">InternetGetProxyInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="72338-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="72338-105">Diese Funktion ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="72338-105">This function is deprecated.</span></span> <span data-ttu-id="72338-106">Verwenden Sie für die aktivierter automatischer Proxy-Unterstützung stattdessen HTTP-Dienste (WinHTTP), Version 5,1.</span><span class="sxs-lookup"><span data-stu-id="72338-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="72338-107">Weitere Informationen finden Sie [unter WinHTTP AutoProxy-Unterstützung](../winhttp/winhttp-autoproxy-support.md).</span><span class="sxs-lookup"><span data-stu-id="72338-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="72338-108">Ruft Proxy Daten für den Zugriff auf angegebene Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="72338-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="72338-109">Diese Funktion kann nur durch dynamisches Verknüpfen mit "JSProxy.dll" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="72338-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="72338-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="72338-110">Syntax</span></span>

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a><span data-ttu-id="72338-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="72338-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72338-112">*lpszurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72338-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72338-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die URL der http-Ziel Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="72338-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="72338-114">*dwurllength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72338-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72338-115">Die Größe (in Bytes) der URL, auf die *lpszurl* zeigt.</span><span class="sxs-lookup"><span data-stu-id="72338-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="72338-116">*lpszurlhostname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72338-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72338-117">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Hostnamen der Ziel-URL angibt.</span><span class="sxs-lookup"><span data-stu-id="72338-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="72338-118">*dwurlhostnamelength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72338-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72338-119">Die Größe (in Bytes) des Host namens, auf den von *lpszurlhostname* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="72338-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="72338-120">*lplpszproxyhostname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72338-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72338-121">Ein Zeiger auf die Adresse eines Puffers, der die URL des Proxys empfängt, der in einer HTTP-Anforderung für die angegebene Ressource verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72338-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="72338-122">Die Anwendung ist dafür verantwortlich, diese Zeichenfolge freizugeben.</span><span class="sxs-lookup"><span data-stu-id="72338-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="72338-123">*lpdwproxyhostnamelength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72338-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72338-124">Ein Zeiger auf eine Variable, die die Größe der Zeichenfolge in Bytes empfängt, die im *lplpszproxyhostname* -Puffer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="72338-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72338-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72338-125">Return value</span></span>

<span data-ttu-id="72338-126">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="72338-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="72338-127">Um erweiterte Fehler Daten abzurufen, nennen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="72338-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="72338-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72338-128">Remarks</span></span>

<span data-ttu-id="72338-129">Um **internetgetproxyinfo** aufzurufen, müssen Sie dynamisch mit dem definierten Funktions Zeigertyp **pfninternetgetproxyinfo** mit ihm verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="72338-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="72338-130">Der folgende Code Ausschnitt zeigt, wie Sie eine Instanz dieses Funktionszeiger Typs deklarieren und anschließend initialisieren und aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="72338-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

<span data-ttu-id="72338-131">Wie alle anderen Aspekte der WinInet-API kann diese Funktion nicht sicher innerhalb von DllMain oder den Konstruktoren und Dekonstruktoren von globalen Objekten aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="72338-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="72338-132">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="72338-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="72338-133">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72338-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="72338-134">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="72338-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="72338-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72338-135">Requirements</span></span>

| <span data-ttu-id="72338-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72338-136">Requirement</span></span> | <span data-ttu-id="72338-137">Wert</span><span class="sxs-lookup"><span data-stu-id="72338-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72338-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72338-138">Minimum supported client</span></span><br/> | <span data-ttu-id="72338-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72338-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72338-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72338-140">Minimum supported server</span></span><br/> | <span data-ttu-id="72338-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72338-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72338-142">DLL</span><span class="sxs-lookup"><span data-stu-id="72338-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72338-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72338-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="72338-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72338-144">See also</span></span>

[<span data-ttu-id="72338-145">**Internetinitializeautoproxydll**</span><span class="sxs-lookup"><span data-stu-id="72338-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="72338-146">[**Internetdeinitializeautoproxydll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="72338-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="72338-147">**Detectautoproxyurl**</span><span class="sxs-lookup"><span data-stu-id="72338-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
