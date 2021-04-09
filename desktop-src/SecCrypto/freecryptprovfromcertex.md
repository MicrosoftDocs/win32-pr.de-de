---
description: 'Gibt das Handle entweder für einen Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) oder für einen CNG-Schlüssel (Cryptography API: Next Generation) frei.'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Freecryptprovfromcertex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867420"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="cd72c-103">Freecryptprovfromcertex-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd72c-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="cd72c-104">Die **freecryptprovfromcertex** -Funktion gibt das Handle entweder für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) oder für einen CNG-Schlüssel (Cryptography API: Next Generation) frei.</span><span class="sxs-lookup"><span data-stu-id="cd72c-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="cd72c-105">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="cd72c-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="cd72c-106">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cd72c-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cd72c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd72c-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="cd72c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd72c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd72c-109">*facettrot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd72c-110">Ein-Wert, der angibt, ob das Anbieter Handle aus dem [*Zertifikat*](../secgloss/c-gly.md)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cd72c-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd72c-111">*hprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd72c-112">Ein Handle für einen CAPICOM-CSP oder ein Handle für einen CNG-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="cd72c-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="cd72c-113">*dwkeyspec*</span><span class="sxs-lookup"><span data-stu-id="cd72c-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="cd72c-114">Die Adresse einer **DWORD** -Variablen, die zusätzliche Informationen über den Schlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="cd72c-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="cd72c-115">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="cd72c-115">This can be one of the following values.</span></span>



| <span data-ttu-id="cd72c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cd72c-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="cd72c-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cd72c-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="cd72c-118"><dt>**bei \_ keyexchange**</dt></span><span class="sxs-lookup"><span data-stu-id="cd72c-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="cd72c-119">Das Schlüsselpaar ist ein Schlüsselaustausch Paar.</span><span class="sxs-lookup"><span data-stu-id="cd72c-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="cd72c-120"><dt>**bei \_ Signatur**</dt></span><span class="sxs-lookup"><span data-stu-id="cd72c-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="cd72c-121">Das Schlüsselpaar ist ein Signatur Paar.</span><span class="sxs-lookup"><span data-stu-id="cd72c-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="cd72c-122"><dt>**Zertifikat- \_ NCrypt- \_ Schlüssel \_ Spezifikation**</dt></span><span class="sxs-lookup"><span data-stu-id="cd72c-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="cd72c-123">Der Schlüssel ist ein CNG-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="cd72c-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="cd72c-124">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd72c-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd72c-125">*pwszcapiprovider* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd72c-126">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Anbieter Namen.</span><span class="sxs-lookup"><span data-stu-id="cd72c-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="cd72c-127">*dwprovidertype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd72c-128">Gibt den CSP-Typ an.</span><span class="sxs-lookup"><span data-stu-id="cd72c-128">Specifies the CSP type.</span></span> <span data-ttu-id="cd72c-129">Dies kann NULL oder einer der [kryptografieanbiettypen](cryptographic-provider-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="cd72c-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="cd72c-130">Wenn dieser Member 0 (null) ist, ist der Schlüssel Container einer der CNG-Schlüsselspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="cd72c-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="cd72c-131">*pwsztmpcontainer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd72c-132">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Namen des temporären Schlüssel Containers.</span><span class="sxs-lookup"><span data-stu-id="cd72c-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd72c-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd72c-133">Return value</span></span>

<span data-ttu-id="cd72c-134">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd72c-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd72c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd72c-135">Requirements</span></span>



| <span data-ttu-id="cd72c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd72c-136">Requirement</span></span> | <span data-ttu-id="cd72c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cd72c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd72c-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd72c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cd72c-139">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cd72c-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd72c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cd72c-141">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd72c-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd72c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cd72c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd72c-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd72c-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
