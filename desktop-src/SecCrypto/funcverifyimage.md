---
description: Wird von einem Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) verwendet, um die Signatur einer DLL zu überprüfen.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE Funktionszeiger (Cspdk.h)
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
ms.openlocfilehash: b33e6e627c87840e4adb7615f7e3ca5932a7402a3b3ae7110be51c0847a5f67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006678"
---
# <a name="crypt_verify_image-function-pointer"></a>CRYPT \_ VERIFY \_ IMAGE-Funktionszeiger

Die **FuncVerifyImage-Rückruffunktion** wird von einem Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) verwendet, um die Signatur einer DLL zu überprüfen.

Alle zusätzlichen DLLs, in denen ein CSP Funktionsaufrufe vorsingt, müssen auf die gleiche Weise (und mit demselben Schlüssel) wie die primäre CSP-DLL signiert werden. Um diese Signatur sicherzustellen, müssen die Hilfs-DLLs dynamisch mithilfe der [**LoadLibrary-Funktion geladen**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) werden. Bevor die DLL geladen wird, muss jedoch die Signatur der DLL überprüft werden. Der CSP führt diese Überprüfung durch, indem er die **Funktion FuncVerifyImage** aufruft, wie im folgenden Beispiel gezeigt.

## <a name="syntax"></a>Syntax


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszImage* \[ In\]
</dt> <dd>

Die Adresse einer auf NULL beendeten Zeichenfolge, die den Pfad und Dateinamen der DLL enthält, für die die Signatur überprüft werden soll.

</dd> <dt>

*pbSigData* \[ In\]
</dt> <dd>

Die Adresse eines Puffers, der die Signatur enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Funktion erfolgreich ist, **FALSE,** wenn sie fehlschlägt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie die **FuncVerifyImage-Rückruffunktion** verwenden, um die Signatur einer DLL zu überprüfen, bevor sie von einem CSP geladen wird.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
