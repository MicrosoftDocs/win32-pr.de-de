---
description: Signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Signersignetx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755561"
---
# <a name="signersignex-function"></a><span data-ttu-id="b768e-103">Signersignetx-Funktion</span><span class="sxs-lookup"><span data-stu-id="b768e-103">SignerSignEx function</span></span>

<span data-ttu-id="b768e-104">Die **signersignetx** -Funktion signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="b768e-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="b768e-105">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b768e-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="b768e-106">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="b768e-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b768e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b768e-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="b768e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b768e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b768e-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b768e-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-110">Ändert das Verhalten dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="b768e-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="b768e-111">Wenn es sich bei der zu Signier enden Datei um eine portable ausführbare Datei (PE) handelt, kann diese 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="b768e-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="b768e-112">Diese Bezeichner sind in "mssip. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="b768e-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="b768e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b768e-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="b768e-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b768e-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="b768e-115"><dt>**SPC \_ Exkl \_ PE \_ \_ Seitenhashes, \_ Flag**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="b768e-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="b768e-116">Ausschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei.</span><span class="sxs-lookup"><span data-stu-id="b768e-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="b768e-117">Dieses Flag hat Vorrang vor dem **Flag "SPC \_ Inc \_ PE \_ \_ Seitenhashes \_** ".</span><span class="sxs-lookup"><span data-stu-id="b768e-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="b768e-118">Wenn weder der Befehl " **SPC \_ EXC \_ PE \_ Page \_ Hashes \_** " noch das Flag " **SPC \_ Inc \_ PE \_ Page \_ Hashes \_** Flag Flag" angegeben ist, wird der mit der [**wintrustsetdefaultincludegpgehashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) -Funktion festgelegte Wert für diese Einstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b768e-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="b768e-119">Der Standardwert für diese Einstellung besteht darin, Seitenhashes auszuschließen, wenn indirekte SIP-Daten für PE-Dateien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b768e-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="b768e-120">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b768e-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="b768e-121"><dt>**SPC \_ Inkl \_ PE \_ Import \_ addr \_ - \_ Tabellenflag**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="b768e-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="b768e-122">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b768e-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="b768e-123"><dt>**SPC \_ Inc \_ PE \_ - \_ debuginfoflag \_**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="b768e-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="b768e-124">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b768e-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="b768e-125"><dt>**SPC \_ Inkl \_ PE \_ Resources- \_ Flag**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="b768e-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="b768e-126">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b768e-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="b768e-127"><dt>**SPC \_ Inkl \_ . \_ \_ Seitenhashes- \_ Flag**</dt> <dt>0x100</dt></span><span class="sxs-lookup"><span data-stu-id="b768e-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="b768e-128">Einschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei.</span><span class="sxs-lookup"><span data-stu-id="b768e-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="b768e-129">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b768e-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="b768e-130">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b768e-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-131">Ein Zeiger auf die [**\_ \_ Info**](signer-subject-info.md) -Struktur des Signatur Gebers, die den Betreff angibt, der signiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b768e-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-132">*psignercert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b768e-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-133">Ein Zeiger auf eine [**Signatur Geber \_**](signer-cert.md) -Zertifikat Struktur, die das Zertifikat angibt, das zum Erstellen der digitalen Signatur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b768e-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-134">*psignatureinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b768e-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-135">Ein Zeiger auf eine [**\_ Signatur \_**](signer-signature-info.md) Informationsstruktur, die Informationen zur digitalen Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="b768e-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-136">*pproviderinfo* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b768e-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-137">Ein Zeiger auf eine Informationsstruktur des [**Signatur Gebers \_ Anbieters \_**](signer-provider-info.md) , die die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum privaten Schlüssel angibt, die zum Erstellen der digitalen Signatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b768e-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="b768e-138">Wenn der Wert dieses Parameters **null** ist, muss der Wert des *psignercert* -Parameters ein Zertifikat angeben, das einem CSP zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b768e-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-139">*pwszhttptimestamp* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b768e-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-140">Die URL eines Zeitstempel Servers.</span><span class="sxs-lookup"><span data-stu-id="b768e-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-141">*psrequest* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b768e-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-142">Ein Zeiger auf ein Array von [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) Strukturen, die einer Signierungs Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b768e-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="b768e-143">Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter keinen gültigen Wert enthält, der nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="b768e-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-144">*psipdata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b768e-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-145">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b768e-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="b768e-146">Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="b768e-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="b768e-147">*ppsignercontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b768e-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b768e-148">Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte [*BLOB*](../secgloss/b-gly.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="b768e-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="b768e-149">Wenn Sie mit der Verwendung der **Signatur Geber- \_ Kontext** Struktur fertig sind, können Sie die Signatur Geber- **\_ Kontext** Struktur durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="b768e-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b768e-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b768e-150">Return value</span></span>

<span data-ttu-id="b768e-151">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b768e-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="b768e-152">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="b768e-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b768e-153">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b768e-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b768e-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b768e-154">Requirements</span></span>



| <span data-ttu-id="b768e-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b768e-155">Requirement</span></span> | <span data-ttu-id="b768e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b768e-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b768e-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b768e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b768e-158">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b768e-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b768e-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b768e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b768e-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b768e-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b768e-161">DLL</span><span class="sxs-lookup"><span data-stu-id="b768e-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b768e-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b768e-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b768e-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b768e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b768e-164">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="b768e-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="b768e-165">**Signerfresignercontext**</span><span class="sxs-lookup"><span data-stu-id="b768e-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
