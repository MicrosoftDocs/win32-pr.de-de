---
description: Ruft ein Handle für einen Kryptografiedienstanbieter (CSP) und eine Schlüssel Spezifikation für einen Zertifikat Kontext ab.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Getcryptprovfromcert-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350128"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="6d2d5-103">Getcryptprovfromcert-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d2d5-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d2d5-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-104">This API is deprecated.</span></span> <span data-ttu-id="6d2d5-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="6d2d5-106">Die **getcryptprovfromcert** -Funktion Ruft ein Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und eine Schlüssel Spezifikation für einen [*Zertifikat*](../secgloss/c-gly.md) Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="6d2d5-107">Verwenden Sie diese Funktion, um Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) des Zertifikat Ausstellers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="6d2d5-108">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="6d2d5-109">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6d2d5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d2d5-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="6d2d5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d2d5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2d5-112">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-113">Das Handle des Fensters, das als Besitzer beliebiger Dialogfelder verwendet werden soll, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="6d2d5-114">Dieser Member wird derzeit nicht verwendet und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="6d2d5-115">Es ist sicher, **null** für diesen Parameter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-116">*pcert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-117">Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur für das Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-118">*phcryptprov* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-119">Ein Zeiger auf eine [**hcryptprov**](hcryptprov.md) -Struktur, die ein Handle für den CSP ist.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-120">*pdwkeyspec* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-121">Die Spezifikation des abzurufenden privaten Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="6d2d5-122">Mögliche Werte sind **bei \_ keyexchange** oder **bei \_ Signatur**.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-123">*pfdidcryptacquire* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-124">Ein-Wert, der angibt, ob die Funktion das Anbieter handle basierend auf dem Zertifikat abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-125">*ppwsztmpcontainer* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-126">Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den temporären Schlüssel Container Namen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="6d2d5-127">Mit der **getcryptprovfromcert** -Funktion wird der temporäre Container bereitstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="6d2d5-128">Beim Aufrufen von **getcryptprovfromcert** sollte die Adresse auf einen **null** -Wert zeigen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-129">*ppwszprovidername* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-130">Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den Anbieter Namen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="6d2d5-131">Die **getcryptprovfromcert** -Funktion gibt den Anbieter Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="6d2d5-132">Beim Aufrufen von **getcryptprovfromcert** sollte die Adresse auf einen **null** -Wert zeigen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="6d2d5-133">*pdwprovidertype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2d5-134">Gibt den CSP-Typ an.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-134">Specifies the CSP type.</span></span> <span data-ttu-id="6d2d5-135">Dies kann NULL oder einer der [kryptografieanbiettypen](cryptographic-provider-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="6d2d5-136">Wenn dieser Member 0 (null) ist, ist der Schlüssel Container einer der CNG-Schlüsselspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2d5-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d2d5-137">Return value</span></span>

<span data-ttu-id="6d2d5-138">Bei Erfolg gibt diese Funktion " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="6d2d5-139">Die **getcryptprovfromcert** -Funktion gibt **false** zurück, wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2d5-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d2d5-140">Remarks</span></span>

<span data-ttu-id="6d2d5-141">Das [Makecert](makecert.md) -Tool ruft **getcryptprovfromcert** auf, wenn Sie es mithilfe der Befehlszeilenoption **-is** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="6d2d5-142">Wenn der Parameter " *pfdidcryptacquire* " auf " **true**" festgelegt ist, legt die Funktion die Parameter " *phcryptprov*", " *pdwkeyspec*" und " *pdwprovidertype* " auf die Anbieter Werte fest.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="6d2d5-143">Wenn Sie die Verwendung des CSP abgeschlossen haben, können Sie es durch Aufrufen der [**freecryptprovfromcert**](freecryptprovfromcert.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="6d2d5-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2d5-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2d5-144">Requirements</span></span>



| <span data-ttu-id="6d2d5-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d2d5-145">Requirement</span></span> | <span data-ttu-id="6d2d5-146">Wert</span><span class="sxs-lookup"><span data-stu-id="6d2d5-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2d5-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d2d5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2d5-148">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6d2d5-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d2d5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2d5-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d2d5-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d2d5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2d5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d2d5-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d2d5-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
