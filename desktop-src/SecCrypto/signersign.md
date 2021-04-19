---
description: Signiert die angegebene Datei.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Signersign-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349340"
---
# <a name="signersign-function"></a><span data-ttu-id="70e96-103">Signersign-Funktion</span><span class="sxs-lookup"><span data-stu-id="70e96-103">SignerSign function</span></span>

<span data-ttu-id="70e96-104">Die **signersign** -Funktion signiert die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="70e96-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="70e96-105">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="70e96-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="70e96-106">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="70e96-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="70e96-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="70e96-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="70e96-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="70e96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e96-109">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70e96-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-110">Ein Zeiger auf die [**\_ \_ Info**](signer-subject-info.md) -Struktur des Signatur Gebers, die den Betreff angibt, der signiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="70e96-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="70e96-111">*psignercert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70e96-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-112">Ein Zeiger auf eine [**Signatur Geber \_**](signer-cert.md) -Zertifikat Struktur, die das Zertifikat angibt, das zum Erstellen der digitalen Signatur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70e96-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="70e96-113">*psignatureinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70e96-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-114">Ein Zeiger auf eine [**\_ Signatur \_**](signer-signature-info.md) Informationsstruktur, die Informationen zur digitalen Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="70e96-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="70e96-115">*pproviderinfo* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="70e96-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-116">Ein Zeiger auf eine Informationsstruktur des [**Signatur Gebers \_ Anbieters \_**](signer-provider-info.md) , die die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum [*privaten Schlüssel*](../secgloss/p-gly.md) angibt, die zum Erstellen der digitalen Signatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70e96-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="70e96-117">Wenn der Wert dieses Parameters **null** ist, muss der Wert des *psignercert* -Parameters ein Zertifikat angeben, das einem CSP zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="70e96-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="70e96-118">*pwszhttptimestamp* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="70e96-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-119">Die URL eines Zeitstempel Servers.</span><span class="sxs-lookup"><span data-stu-id="70e96-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="70e96-120">*psrequest* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="70e96-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-121">Ein Zeiger auf ein Array von [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) Strukturen, die einer Signierungs Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="70e96-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="70e96-122">Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter keinen gültigen Wert enthält, der nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="70e96-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="70e96-123">*psipdata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="70e96-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e96-124">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="70e96-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="70e96-125">Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="70e96-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e96-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70e96-126">Return value</span></span>

<span data-ttu-id="70e96-127">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="70e96-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="70e96-128">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="70e96-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="70e96-129">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="70e96-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70e96-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70e96-130">Requirements</span></span>



| <span data-ttu-id="70e96-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70e96-131">Requirement</span></span> | <span data-ttu-id="70e96-132">Wert</span><span class="sxs-lookup"><span data-stu-id="70e96-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70e96-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70e96-133">Minimum supported client</span></span><br/> | <span data-ttu-id="70e96-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70e96-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="70e96-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70e96-135">Minimum supported server</span></span><br/> | <span data-ttu-id="70e96-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70e96-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70e96-137">DLL</span><span class="sxs-lookup"><span data-stu-id="70e96-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70e96-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70e96-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e96-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70e96-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e96-140">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="70e96-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
