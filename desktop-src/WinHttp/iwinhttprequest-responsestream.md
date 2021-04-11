---
description: Ruft den Entitäts Text der Antwort als IStream ab.
ms.assetid: e12a9338-5e0c-4672-bbc6-31375b872e94
title: 'Iwinhttprequest:: Response Stream-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseStream
- IWinHttpRequest.get_ResponseStream
- WinHttpRequest.ResponseStream
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ec9f497e687c52735784a5e3edad01905ac7a6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217410"
---
# <a name="iwinhttprequestresponsestream-property"></a>Iwinhttprequest:: Response Stream-Eigenschaft

Die Response **Stream** -Eigenschaft ruft den Entitäts Text der Antwort als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ResponseStream(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseStream = WinHttpRequest.ResponseStream
```





## <a name="property-value"></a>Eigenschaftswert

Eine **Variante** , die einen Zeiger auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle empfängt, die für eine [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle abgefragt werden kann. Dieser Stream gibt die Rohdaten zurück, die vom Server direkt empfangen werden.

## <a name="error-codes"></a>Fehlercodes

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

Wenn der vorherige [**Sende**](iwinhttprequest-send.md) Vorgang nicht abgeschlossen ist, wird **E \_ Ausstehend** angezeigt.

## <a name="remarks"></a>Bemerkungen

Rufen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den zurückgegebenen Zeiger auf, um einen Zeiger auf eine [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle zu erhalten. Diese Eigenschaft gibt die Antwortdaten als **IStream** zurück. Diese Eigenschaft kann nur aufgerufen werden, nachdem die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wurde.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie eine HTTP-Verbindung geöffnet, eine HTTP-Anforderung gesendet und die Antwort als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)gelesen wird. Die Daten aus dem **IStream** werden in die Datei Temp1.gif geschrieben.


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

#define Trace(_s) fprintf(stderr, _s) 
#define TraceErr(_s, _hr) fprintf(stderr, _s, _hr) 
#define Check(_hr,_s) if (FAILED(_hr)) { fprintf(stderr, _s ## " 0x%08lx\n", _hr); return -1; }

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    // Variable for return value.
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT            varResponse;

    VariantInit(&varResponse);
    
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

    // ==== Get binary (.gif) file and write it to disk. =========
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get response body.
        hr = pIWinHttpRequest->get_ResponseBody(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        long UpperBounds;
        long LowerBounds;
        unsigned char* buff;
        // Verify that varResponse contains array of unsigned bytes.
        if (varResponse.vt == (VT_ARRAY | VT_UI1)) {
            long Dims = SafeArrayGetDim(varResponse.parray);
            // The array should only have 1 dimension.
            if (Dims == 1) {
                // Get upper and lower array bounds.
                SafeArrayGetLBound(varResponse.parray, 1, 
                                   &LowerBounds);
                SafeArrayGetUBound(varResponse.parray, 1, 
                                   &UpperBounds);
                UpperBounds++;
                // Lock SAFEARRAY for access.
                SafeArrayAccessData (varResponse.parray, 
                                     (void**)&buff);
                // Output array to file temp.gif.
                HANDLE hFile; 
                DWORD  dwBytesWritten;
                // Create file.
                hFile = CreateFile(TEXT("Temp1.gif"),     
                    GENERIC_WRITE,              // Open for writing. 
                    0,                          // Do not share. 
                    NULL,                       // No security. 
                    CREATE_ALWAYS,              // Overwrite existing.
                    FILE_ATTRIBUTE_NORMAL,      // Normal file.
                    NULL);                      // No attribute template.

                if (hFile == INVALID_HANDLE_VALUE) 
                    {
                    wprintf(L"Could not open file."); // Process error.
                    }
                else
                    {
                    WriteFile(hFile, buff, UpperBounds - LowerBounds, 
                        &dwBytesWritten, NULL); 
                    }
                CloseHandle(hFile);
                SafeArrayUnaccessData (varResponse.parray);
            }
        }    
    }

    // ======== Get binary (.gif) file and write 
    // it to disk using IStream. ================
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response as an IStream.
        hr = pIWinHttpRequest->get_ResponseStream(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        IStream*    pStream = NULL; 
        BYTE        bBuffer[8192]; 
        DWORD       cb, cbRead, cbWritten; 
        // Check that an IStream was received.
        if (VT_UNKNOWN == V_VT(&varResponse) || 
            VT_STREAM == V_VT(&varResponse)) 
        { 
            // Get IStream interface pStream.
            hr = V_UNKNOWN(&varResponse)->QueryInterface(IID_IStream, 
                                 reinterpret_cast<void**>(&pStream)); 
            Check(hr, "QI for IStream"); 
        } 
        else 
        { 
            wprintf(L"Unexpected vartype for Response\n"); 
            return -1; 
        } 

        HANDLE hFile; 
        // Open file Temp2.gif for output.
        hFile = CreateFile(TEXT("Temp2.gif"),     
            GENERIC_WRITE,                // Open for writing. 
            0,                            // Do not share. 
            NULL,                         // No security. 
            CREATE_ALWAYS,                // Overwrite existing.
            FILE_ATTRIBUTE_NORMAL,        // Normal file.
            NULL);                        // No attribute template.
        if (hFile == INVALID_HANDLE_VALUE) 
            {
            wprintf(L"Could not open file.");  // Process error.
            }
        else
            {
            // Copy data from the response stream to file. 
            cb = sizeof(bBuffer); 
            hr = pStream->Read(bBuffer, cb, &cbRead); 
            while (SUCCEEDED(hr) && 0 != cbRead) 
                { 
                if (!WriteFile(hFile, bBuffer, 
                               cbRead, &cbWritten, NULL)) 
                    { 
                    TraceErr("WriteFile fails with 0x%08lx\n", 
                             HRESULT_FROM_WIN32(GetLastError())); 
                    return -1; 
                    } 
                hr = pStream->Read(bBuffer, cb, &cbRead); 
                } 
            }
        CloseHandle(hFile);
        pStream->Release(); 
        VariantClear(&varResponse); 
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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwinhttprequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**Response Body**](iwinhttprequest-responsebody.md)
</dt> <dt>

[**Response Text**](iwinhttprequest-responsetext.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

