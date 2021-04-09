---
description: Gibt das Handle für einen Kryptografiedienstanbieter (CSP) frei und löscht optional den temporären Container, der von der getcryptprovfromcert-Funktion erstellt wurde.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Freecryptprovfromcert-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867423"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="7b5a0-103">Freecryptprovfromcert-Funktion</span><span class="sxs-lookup"><span data-stu-id="7b5a0-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b5a0-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-104">This API is deprecated.</span></span> <span data-ttu-id="7b5a0-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="7b5a0-106">Die Funktion **freecryptprovfromcert** gibt das Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) frei und löscht optional den temporären Container, der von der [**getcryptprovfromcert**](getcryptprovfromcert.md) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="7b5a0-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="7b5a0-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7b5a0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b5a0-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="7b5a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b5a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b5a0-111">*facettrot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a0-112">Ein-Wert, der angibt, ob das Anbieter Handle aus dem [*Zertifikat*](../secgloss/c-gly.md)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b5a0-113">*hprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a0-114">Ein Zeiger auf eine [**hcryptprov**](hcryptprov.md) -Struktur für den CSP.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="7b5a0-115">*pwszcapiprovider* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a0-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Anbieter Namen.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="7b5a0-117">*dwprovidertype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a0-118">Gibt den CSP-Typ an.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-118">Specifies the CSP type.</span></span> <span data-ttu-id="7b5a0-119">Dies kann NULL oder einer der [kryptografieanbiettypen](cryptographic-provider-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="7b5a0-120">Wenn dieser Member 0 (null) ist, ist der Schlüssel Container einer der CNG-Schlüsselspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="7b5a0-121">*pwsztmpcontainer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a0-122">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Namen des temporären Schlüssel Containers.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b5a0-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b5a0-123">Return value</span></span>

<span data-ttu-id="7b5a0-124">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7b5a0-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5a0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b5a0-125">Requirements</span></span>



| <span data-ttu-id="7b5a0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b5a0-126">Requirement</span></span> | <span data-ttu-id="7b5a0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7b5a0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5a0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b5a0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5a0-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7b5a0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b5a0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5a0-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b5a0-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b5a0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7b5a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b5a0-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b5a0-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
