---
description: Gibt das Handle für einen Kryptografiedienstanbieter (CSP) frei und löscht optional den temporären Container, der von der pvkgetcryptprov-Funktion erstellt wurde.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Pvkfreecryptprov-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349657"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="24f2c-103">Pvkfreecryptprov-Funktion</span><span class="sxs-lookup"><span data-stu-id="24f2c-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24f2c-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="24f2c-104">This API is deprecated.</span></span> <span data-ttu-id="24f2c-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="24f2c-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="24f2c-106">Die **pvkfreecryptprov** -Funktion gibt das Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) frei und löscht optional den temporären Container, der von der Funktion [**pvkgetcryptprov**](pvkgetcryptprov.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="24f2c-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="24f2c-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="24f2c-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="24f2c-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="24f2c-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="24f2c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="24f2c-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="24f2c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24f2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f2c-111">*hprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f2c-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f2c-112">Ein Handle für den CSP.</span><span class="sxs-lookup"><span data-stu-id="24f2c-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="24f2c-113">*pwszcapiprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f2c-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f2c-114">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den CSP-Namen.</span><span class="sxs-lookup"><span data-stu-id="24f2c-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="24f2c-115">*dwprovidertype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f2c-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f2c-116">Ein **DWORD** -Wert, der den Typ des Kryptografieanbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="24f2c-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="24f2c-117">Weitere Informationen finden Sie unter [Typen von Kryptografieanbietern](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="24f2c-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="24f2c-118">*pwsztmpcontainer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="24f2c-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24f2c-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den temporären Schlüssel Container Namen.</span><span class="sxs-lookup"><span data-stu-id="24f2c-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f2c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24f2c-120">Return value</span></span>

<span data-ttu-id="24f2c-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24f2c-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f2c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24f2c-122">Requirements</span></span>



| <span data-ttu-id="24f2c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24f2c-123">Requirement</span></span> | <span data-ttu-id="24f2c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="24f2c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f2c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24f2c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="24f2c-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24f2c-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="24f2c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24f2c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="24f2c-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24f2c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24f2c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="24f2c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24f2c-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24f2c-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
