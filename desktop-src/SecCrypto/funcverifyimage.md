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
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="9a5f0-103">Crypt \_ - \_ Bild Funktionszeiger überprüfen</span><span class="sxs-lookup"><span data-stu-id="9a5f0-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="9a5f0-104">Die **funkverifyimage** -Rückruffunktion wird von einem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zum Überprüfen der Signatur einer DLL verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="9a5f0-105">Alle Erweiterungs-DLLs, in die ein CSP Funktionsaufrufe durchführt, müssen auf die gleiche Weise (und mit demselben Schlüssel) wie die primäre CSP-DLL signiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="9a5f0-106">Um diese Signatur sicherzustellen, müssen die zusätzlichen DLLs dynamisch mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="9a5f0-107">Aber bevor die dll geladen wird, muss die Signatur der dll überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="9a5f0-108">Der CSP führt diese Überprüfung durch Aufrufen der Funktion **funcverifyimage** aus, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5f0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a5f0-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="9a5f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a5f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a5f0-111">*lpszimage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a5f0-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a5f0-112">Die Adresse einer auf NULL endenden Zeichenfolge, die den Pfad und den Dateinamen der dll enthält, für die die Signatur überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="9a5f0-113">*pbsigdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a5f0-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a5f0-114">Die Adresse eines Puffers, der die Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a5f0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a5f0-115">Return value</span></span>

<span data-ttu-id="9a5f0-116">Gibt **true** zurück, wenn die Funktion erfolgreich ist, und **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="9a5f0-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a5f0-117">Examples</span></span>

<span data-ttu-id="9a5f0-118">Im folgenden Beispiel wird gezeigt, wie Sie die Funktion " **funcverifyimage** " verwenden, um die Signatur einer DLL zu überprüfen, bevor Sie von einem CSP geladen wird.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9a5f0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a5f0-119">Requirements</span></span>



| <span data-ttu-id="9a5f0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a5f0-120">Requirement</span></span> | <span data-ttu-id="9a5f0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9a5f0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5f0-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a5f0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a5f0-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a5f0-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a5f0-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a5f0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a5f0-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a5f0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9a5f0-126">Header</span><span class="sxs-lookup"><span data-stu-id="9a5f0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a5f0-127"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a5f0-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a5f0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a5f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5f0-129">**Cpacquirecontext**</span><span class="sxs-lookup"><span data-stu-id="9a5f0-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="9a5f0-130">**Vtableprovstruc**</span><span class="sxs-lookup"><span data-stu-id="9a5f0-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
