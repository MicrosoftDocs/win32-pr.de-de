---
description: Speichert einen privaten Schlüssel und den zugehörigen öffentlichen Schlüssel in einer angegebenen Datei.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Pvkprivatekeysave-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351815"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="39480-103">Pvkprivatekeysave-Funktion</span><span class="sxs-lookup"><span data-stu-id="39480-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39480-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="39480-104">This API is deprecated.</span></span> <span data-ttu-id="39480-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="39480-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="39480-106">Die **pvkprivatekeysave** -Funktion speichert einen [*privaten Schlüssel*](../secgloss/p-gly.md) und den zugehörigen [*öffentlichen Schlüssel*](../secgloss/p-gly.md) in einer angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="39480-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="39480-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="39480-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="39480-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="39480-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="39480-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="39480-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="39480-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39480-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39480-111">*hcryptprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39480-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39480-112">Ein Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="39480-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="39480-113">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39480-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39480-114">Ein Handle für eine Datei, die mit der ersten Lese-/Schreibberechtigung und einer nachfolgenden schreibgeschützten Berechtigung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="39480-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="39480-115">*dwkeyspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39480-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39480-116">Eine lange ganze Zahl für den Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="39480-116">A long integer for the type of key.</span></span> <span data-ttu-id="39480-117">Mögliche Werte sind **bei \_ keyexchange** oder **bei \_ Signatur**.</span><span class="sxs-lookup"><span data-stu-id="39480-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="39480-118">*hwndOwner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39480-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39480-119">Wenn ein Kennwort zum Verschlüsseln des privaten Schlüssels erforderlich ist, ist dieser Parameter ein Handle für das übergeordnete Element des Dialog Felds. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="39480-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39480-120">*pwszkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39480-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39480-121">Ein Zeiger auf eine mit NULL endende Zeichenfolge für den Namen des zu speichernden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="39480-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="39480-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39480-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39480-123">Ein **DWORD** -Wert, der zusätzliche Optionen für die Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="39480-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="39480-124">Weitere Informationen finden Sie unter dem *dwFlags* -Parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="39480-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39480-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39480-125">Return value</span></span>

<span data-ttu-id="39480-126">Bei Erfolg gibt diese Funktion " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="39480-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="39480-127">Die **pvkprivatekeysave** -Funktion gibt **false** zurück, wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="39480-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="39480-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39480-128">Requirements</span></span>



| <span data-ttu-id="39480-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39480-129">Requirement</span></span> | <span data-ttu-id="39480-130">Wert</span><span class="sxs-lookup"><span data-stu-id="39480-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39480-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39480-131">Minimum supported client</span></span><br/> | <span data-ttu-id="39480-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39480-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="39480-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39480-133">Minimum supported server</span></span><br/> | <span data-ttu-id="39480-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39480-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39480-135">DLL</span><span class="sxs-lookup"><span data-stu-id="39480-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39480-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39480-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
