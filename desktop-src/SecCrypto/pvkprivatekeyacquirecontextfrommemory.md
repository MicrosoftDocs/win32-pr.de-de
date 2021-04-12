---
description: Erstellt einen temporären Container im Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) und lädt einen privaten Schlüssel aus dem Arbeitsspeicher in den Container.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: Pvkprivatekeyacquirecontextfrommemory-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348488"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="cdd97-103">Pvkprivatekeyacquirecontextfrommemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdd97-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdd97-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cdd97-104">This API is deprecated.</span></span> <span data-ttu-id="cdd97-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="cdd97-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="cdd97-106">Die **pvkprivatekeyacquirecontextfrommemory** -Funktion erstellt einen temporären Container im [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) und lädt einen [*privaten Schlüssel*](../secgloss/p-gly.md) aus dem Arbeitsspeicher in den Container.</span><span class="sxs-lookup"><span data-stu-id="cdd97-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="cdd97-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="cdd97-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="cdd97-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cdd97-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cdd97-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd97-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="cdd97-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd97-111">*pwszprovname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des CSP enthält, dessen Typ in *dwprovtype* angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="cdd97-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-113">*dwprovtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-114">Ein **DWORD** -Wert für den CSP-Typ.</span><span class="sxs-lookup"><span data-stu-id="cdd97-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="cdd97-115">Weitere Informationen zu CSP-Typen finden Sie unter [Typen von Kryptografieanbietern](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-116">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-117">Ein Zeiger auf einen Puffer, um die Kontext Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="cdd97-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="cdd97-118">Der Aufrufer muss diese Ressource bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cdd97-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-119">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-120">Ein **DWORD** -Wert, der die Größe des *pbData* -Puffers in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="cdd97-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="cdd97-121">Der Aufrufer muss diesen Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="cdd97-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-122">*hwndOwner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-123">Wenn ein Kennwort zum Entschlüsseln der Kontext Daten erforderlich ist, auf die durch den *pbData* -Parameter verwiesen wird, ist dieser Parameter ein Handle für das übergeordnete Dialogfeld. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="cdd97-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-124">*pwszkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-125">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des abzurufenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="cdd97-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-126">*pdwkeyspec* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-127">Ein Zeiger auf einen **DWORD** -Wert, der den Typ des Schlüssels angibt.</span><span class="sxs-lookup"><span data-stu-id="cdd97-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="cdd97-128">Mögliche Werte sind **bei \_ keyexchange** oder **bei \_ Signatur**.</span><span class="sxs-lookup"><span data-stu-id="cdd97-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-129">*phcryptprov* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-130">Ein Zeiger auf ein Handle für den CSP.</span><span class="sxs-lookup"><span data-stu-id="cdd97-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-131">*ppwsztmpcontainer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd97-132">Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den temporären Container Namen.</span><span class="sxs-lookup"><span data-stu-id="cdd97-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="cdd97-133">Die **pvkprivatekeyacquirecontextfrommemory** -Funktion stellt den Puffer für diese Zeichenfolge bereit und initialisiert sie.</span><span class="sxs-lookup"><span data-stu-id="cdd97-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="cdd97-134">Beim Aufrufen von **pvkprivatekeyacquirecontextfrommemory** sollte die Adresse auf einen **null** -Wert zeigen.</span><span class="sxs-lookup"><span data-stu-id="cdd97-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd97-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdd97-135">Return value</span></span>

<span data-ttu-id="cdd97-136">Bei Erfolg gibt diese Funktion " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd97-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="cdd97-137">Die **pvkprivatekeyacquirecontextfrommemory** -Funktion gibt **false** zurück, wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cdd97-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd97-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdd97-138">Requirements</span></span>



| <span data-ttu-id="cdd97-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdd97-139">Requirement</span></span> | <span data-ttu-id="cdd97-140">Wert</span><span class="sxs-lookup"><span data-stu-id="cdd97-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd97-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdd97-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd97-142">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cdd97-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdd97-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd97-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdd97-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cdd97-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd97-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd97-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdd97-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
