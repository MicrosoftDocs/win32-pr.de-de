---
title: TF_InvalidAssemblyListCacheIfExist-Funktion
description: Die TF \_ invalidassemblylistcacheifiexist-Funktion macht den Beschreibungs Cache des Texteingabe Prozessors ungültig.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- TF_InvalidAssemblyListCacheIfExist Function-Framework für Text Dienste
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517570"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="eb4af-104">TF \_ invalidassemblylistcacheif exist-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb4af-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="eb4af-105">Die **tf \_ invalidassemblylistcacheifiexist** -Funktion macht den Beschreibungs Cache des Texteingabe Prozessors ungültig.</span><span class="sxs-lookup"><span data-stu-id="eb4af-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="eb4af-106">Es ist nicht erforderlich, diese Funktion aufzurufen, wenn Sie für das Installationsprogramm des Eingabe Prozessors einen Neustart oder eine Anmeldung benötigen.</span><span class="sxs-lookup"><span data-stu-id="eb4af-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="eb4af-107">Der Cache ist gültig, bis der Benutzer sich abmeldet.</span><span class="sxs-lookup"><span data-stu-id="eb4af-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4af-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb4af-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="eb4af-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb4af-109">Parameters</span></span>

<span data-ttu-id="eb4af-110">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eb4af-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb4af-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb4af-111">Return value</span></span>

<span data-ttu-id="eb4af-112">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb4af-112">This function can return one of these values.</span></span>



| <span data-ttu-id="eb4af-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eb4af-113">Return code</span></span>                                                                            | <span data-ttu-id="eb4af-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb4af-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="eb4af-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4af-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="eb4af-116">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="eb4af-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="eb4af-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4af-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="eb4af-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eb4af-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="eb4af-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb4af-119">Examples</span></span>

<span data-ttu-id="eb4af-120">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb4af-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="eb4af-121">Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eb4af-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="eb4af-122">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="eb4af-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="eb4af-123">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="eb4af-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="eb4af-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb4af-124">Requirements</span></span>



| <span data-ttu-id="eb4af-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb4af-125">Requirement</span></span> | <span data-ttu-id="eb4af-126">Wert</span><span class="sxs-lookup"><span data-stu-id="eb4af-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4af-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb4af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4af-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb4af-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="eb4af-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb4af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4af-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb4af-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eb4af-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="eb4af-131">Redistributable</span></span><br/>          | <span data-ttu-id="eb4af-132">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eb4af-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="eb4af-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eb4af-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb4af-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb4af-134"><dt>Msctf.dll</dt></span></span> </dl> |



 

