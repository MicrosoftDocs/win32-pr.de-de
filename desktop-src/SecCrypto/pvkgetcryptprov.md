---
description: Ruft ein Handle für einen Kryptografiedienstanbieter (CSP) basierend auf einer Datei mit einem privaten Schlüssel oder einem Schlüssel Container Namen ab.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Pvkgetcryptprov-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869000"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="62c64-103">Pvkgetcryptprov-Funktion</span><span class="sxs-lookup"><span data-stu-id="62c64-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62c64-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="62c64-104">This API is deprecated.</span></span> <span data-ttu-id="62c64-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="62c64-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="62c64-106">Die **pvkgetcryptprov** -Funktion Ruft ein Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) basierend auf einer Datei mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) oder einem Schlüssel Container Namen ab.</span><span class="sxs-lookup"><span data-stu-id="62c64-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="62c64-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="62c64-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="62c64-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="62c64-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="62c64-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="62c64-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="62c64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="62c64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c64-111">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c64-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-112">Wenn ein Kennwort erforderlich ist, um die Datei mit dem privaten Schlüssel zu entschlüsseln, ist dieser Parameter ein Handle für das übergeordnete Element des Kennwort-Dialog Felds. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="62c64-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-113">*pwszcaption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c64-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-114">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für die Dialogfeld Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="62c64-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-115">*pwszcapiprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c64-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den CSP-Namen.</span><span class="sxs-lookup"><span data-stu-id="62c64-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-117">*dwprovidertype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c64-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-118">Ein **DWORD** -Wert, der den Typ des Kryptografieanbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="62c64-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="62c64-119">Weitere Informationen finden Sie unter [Typen von Kryptografieanbietern](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="62c64-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="62c64-120">*pwszpvkfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c64-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-121">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen einer Datei mit einem privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="62c64-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-122">*pwszkeycontainername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c64-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-123">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Namen des privaten Schlüssel Containers.</span><span class="sxs-lookup"><span data-stu-id="62c64-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-124">*pdwkeyspec* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62c64-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-125">Ein Zeiger auf einen **DWORD** -Wert für den Typ des Schlüssels des Containers, der mit " *phcryptprov* " und " *ppwsztmpcontainer*" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="62c64-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-126">*ppwsztmpcontainer* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="62c64-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-127">Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den temporären Schlüssel Container Namen.</span><span class="sxs-lookup"><span data-stu-id="62c64-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="62c64-128">Die **pvkgetcryptprov** -Funktion stellt den temporären Container bereit und initialisiert diesen.</span><span class="sxs-lookup"><span data-stu-id="62c64-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="62c64-129">Wenn **pvkgetcryptprov** aufgerufen wird, sollte die Adresse auf einen **null** -Wert zeigen.</span><span class="sxs-lookup"><span data-stu-id="62c64-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="62c64-130">*phcryptprov* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62c64-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62c64-131">Ein Zeiger auf ein Handle für den CSP.</span><span class="sxs-lookup"><span data-stu-id="62c64-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c64-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62c64-132">Return value</span></span>

<span data-ttu-id="62c64-133">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="62c64-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="62c64-134">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="62c64-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="62c64-135">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="62c64-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62c64-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62c64-136">Remarks</span></span>

<span data-ttu-id="62c64-137">Die **pvkgetcryptprov** -Funktion versucht zunächst, das Anbieter Handle aus dem Schlüssel Container Namen zu erhalten, der durch den *pwszkeycontainername* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="62c64-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="62c64-138">Wenn Sie **null** für den *pwszkeycontainername* -Parameter übergeben, versucht **pvkgetcryptprov** , den Anbieter aus der Datei mit dem privaten Schlüssel zu erhalten, die im *pwszpvkfile* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="62c64-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="62c64-139">Wenn Sie die Verwendung des CSP abgeschlossen haben, können Sie das Anbieter Handle und den temporären Schlüssel Container durch Aufrufen der [**pvkfreecryptprov**](pvkfreecryptprov.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="62c64-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c64-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62c64-140">Requirements</span></span>



| <span data-ttu-id="62c64-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62c64-141">Requirement</span></span> | <span data-ttu-id="62c64-142">Wert</span><span class="sxs-lookup"><span data-stu-id="62c64-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c64-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62c64-143">Minimum supported client</span></span><br/> | <span data-ttu-id="62c64-144">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62c64-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="62c64-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62c64-145">Minimum supported server</span></span><br/> | <span data-ttu-id="62c64-146">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62c64-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62c64-147">DLL</span><span class="sxs-lookup"><span data-stu-id="62c64-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c64-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c64-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
