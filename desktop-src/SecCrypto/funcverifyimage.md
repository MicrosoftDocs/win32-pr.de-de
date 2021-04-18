---
description: Wird von einem Kryptografiedienstanbieter (CSP) zum Überprüfen der Signatur einer DLL verwendet.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE Funktionszeiger (cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359076"
---
# <a name="crypt_verify_image-function-pointer"></a>Crypt \_ - \_ Bild Funktionszeiger überprüfen

Die **funkverifyimage** -Rückruffunktion wird von einem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zum Überprüfen der Signatur einer DLL verwendet.

Alle Erweiterungs-DLLs, in die ein CSP Funktionsaufrufe durchführt, müssen auf die gleiche Weise (und mit demselben Schlüssel) wie die primäre CSP-DLL signiert werden. Um diese Signatur sicherzustellen, müssen die zusätzlichen DLLs dynamisch mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion geladen werden. Aber bevor die dll geladen wird, muss die Signatur der dll überprüft werden. Der CSP führt diese Überprüfung durch Aufrufen der Funktion **funcverifyimage** aus, wie im folgenden Beispiel gezeigt.

## <a name="syntax"></a>Syntax


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszimage* \[ in\]
</dt> <dd>

Die Adresse einer auf NULL endenden Zeichenfolge, die den Pfad und den Dateinamen der dll enthält, für die die Signatur überprüft werden soll.

</dd> <dt>

*pbsigdata* \[ in\]
</dt> <dd>

Die Adresse eines Puffers, der die Signatur enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Funktion erfolgreich ist, und **false** , wenn Sie fehlschlägt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie die Funktion " **funcverifyimage** " verwenden, um die Signatur einer DLL zu überprüfen, bevor Sie von einem CSP geladen wird.


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpacquirecontext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**Vtableprovstruc**](vtableprovstruc.md)
</dt> </dl>

 

 
