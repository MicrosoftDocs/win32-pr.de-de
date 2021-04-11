---
description: Signiert und Zeitstempel der angegebenen Datei, sodass mehrere Unterschriften zugelassen werden.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217618"
---
# <a name="signersignex2-function"></a><span data-ttu-id="850a6-103">SignerSignEx2-Funktion</span><span class="sxs-lookup"><span data-stu-id="850a6-103">SignerSignEx2 function</span></span>

<span data-ttu-id="850a6-104">Die **SignerSignEx2** -Funktion signiert und Zeitstempel für die angegebene Datei, sodass mehrere unterschiedliche Signaturen möglich sind.</span><span class="sxs-lookup"><span data-stu-id="850a6-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="850a6-105">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="850a6-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="850a6-106">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="850a6-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="850a6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="850a6-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="850a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="850a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="850a6-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="850a6-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-110">Ändert das Verhalten dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="850a6-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="850a6-111">Wenn es sich bei der zu Signier enden Datei um eine portable ausführbare Datei (PE) handelt, kann diese 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="850a6-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="850a6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="850a6-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="850a6-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="850a6-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="850a6-114"><dt>**SPC \_ Exkl \_ PE \_ \_ Seitenhashes, \_ Flag**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="850a6-115">Ausschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei.</span><span class="sxs-lookup"><span data-stu-id="850a6-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="850a6-116">Dieses Flag hat Vorrang vor dem **Flag "SPC \_ Inc \_ PE \_ \_ Seitenhashes \_** ".</span><span class="sxs-lookup"><span data-stu-id="850a6-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="850a6-117">Wenn weder der Befehl " **SPC \_ EXC \_ PE \_ Page \_ Hashes \_** " noch das Flag " **SPC \_ Inc \_ PE \_ Page \_ Hashes \_** Flag Flag" angegeben ist, wird der mit der [**wintrustsetdefaultincludegpgehashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) -Funktion festgelegte Wert für diese Einstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="850a6-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="850a6-118">Der Standardwert für diese Einstellung besteht darin, Seitenhashes auszuschließen, wenn indirekte SIP-Daten für PE-Dateien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="850a6-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="850a6-119">Dieser Wert wird in der Header Datei "mssip. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="850a6-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="850a6-120">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="850a6-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="850a6-121"><dt>**SPC \_ Inkl \_ PE \_ Import \_ addr \_ - \_ Tabellenflag**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="850a6-122">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="850a6-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="850a6-123"><dt>**SPC \_ Inc \_ PE \_ - \_ debuginfoflag \_**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="850a6-124">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="850a6-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="850a6-125"><dt>**SPC \_ Inkl \_ PE \_ Resources- \_ Flag**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="850a6-126">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="850a6-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="850a6-127"><dt>**SPC \_ Inkl \_ . \_ \_ Seitenhashes- \_ Flag**</dt> <dt>0x100</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="850a6-128">Einschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei.</span><span class="sxs-lookup"><span data-stu-id="850a6-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="850a6-129">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="850a6-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="850a6-130">Dieser Wert wird in der Header Datei "mssip. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="850a6-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="850a6-131"><dt>**Sig \_**</dt> <dt>0x1000</dt> anfügen</span><span class="sxs-lookup"><span data-stu-id="850a6-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="850a6-132">Die Signatur wird eingefügt.</span><span class="sxs-lookup"><span data-stu-id="850a6-132">The signature will be nested.</span></span> <span data-ttu-id="850a6-133">Wenn Sie dieses Flag festlegen, bevor eine Signatur hinzugefügt wurde, wird die generierte Signatur als äußere Signatur hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="850a6-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="850a6-134">Wenn Sie dieses Flag nicht festlegen, ersetzt die generierte Signatur die äußere Signatur, wobei alle inneren Signaturen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="850a6-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="850a6-135">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="850a6-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-136">Ein Zeiger auf die [**\_ \_ Informations**](signer-subject-info.md) Struktur des Signatur Gebers, die den Betreff angibt, der signiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="850a6-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-137">*psignercert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="850a6-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-138">Zeiger auf eine [**Signatur Geber- \_ CERT**](signer-cert.md) -Struktur, die das Zertifikat angibt, das zum Erstellen der digitalen Signatur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="850a6-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-139">*psignatureinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="850a6-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-140">Ein Zeiger auf eine [**\_ Signatur \_**](signer-signature-info.md) Informationsstruktur, die Informationen zur digitalen Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="850a6-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-141">*pproviderinfo* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-142">Zeiger auf eine Informationsstruktur des [**Signatur Gebers \_ Anbieters \_**](signer-provider-info.md) , die die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum privaten Schlüssel angibt, die zum Erstellen der digitalen Signatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="850a6-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="850a6-143">Wenn der Wert dieses Parameters **null** ist, muss der *psignercert* -Parameter ein Zertifikat angeben, das einem CSP zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="850a6-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-144">*dwtimestampflags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-145">Flags, die an [**SignerTimeStampEx3**](signertimestampex3.md) übergeben werden, wenn der *pwszhttptimestamp* -Parameter nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="850a6-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="850a6-146">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="850a6-146">This can be one of the following values.</span></span>



| <span data-ttu-id="850a6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="850a6-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="850a6-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="850a6-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="850a6-149"><dt>**Signatur Geber- \_ Zeitstempel \_ Authenticode**</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="850a6-150">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="850a6-150">Default value.</span></span> <span data-ttu-id="850a6-151">Gibt einen Authenticode-Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="850a6-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="850a6-152"><dt>**Signatur Geber- \_ Zeitstempel \_ Timestampserver**</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="850a6-153">Gibt einen RFC 3161-Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="850a6-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="850a6-154">Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter **null** ist.</span><span class="sxs-lookup"><span data-stu-id="850a6-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-155">*psztimestampalgorithmuid* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-156">Der Objekt Bezeichner des Algorithmus, der zum Erstellen eines RFC 3161-Zeitstempels verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="850a6-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="850a6-157">Dieser Parameter wird bei Authenticode-Zeitstempeln ignoriert.</span><span class="sxs-lookup"><span data-stu-id="850a6-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-158">*pwszhttptimestamp* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-159">Die URL des Zeitstempel Servers.</span><span class="sxs-lookup"><span data-stu-id="850a6-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-160">*psrequest* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-161">Zeiger auf ein Array von [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) Strukturen, die einer Signierungs Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="850a6-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="850a6-162">Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter keinen gültigen Wert enthält oder **null** ist.</span><span class="sxs-lookup"><span data-stu-id="850a6-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-163">*psipdata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-164">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="850a6-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="850a6-165">Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="850a6-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-166">*ppsignercontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="850a6-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-167">Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte [*BLOB*](../secgloss/b-gly.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="850a6-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="850a6-168">Wenn Sie mit der Verwendung der **Signatur Geber- \_ Kontext** Struktur fertig sind, können Sie die Signatur Geber- **\_ Kontext** Struktur durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="850a6-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-169">*pcryptopolicy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="850a6-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="850a6-170">Falls vorhanden, ein Zeiger auf eine [**CERT \_ Strong \_ Sign \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) Structure-Struktur, die die Parameter enthält, die für die Überprüfung auf starke Signaturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="850a6-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="850a6-171">Wenn entweder ein Zertifikat oder die zugehörige Kette nicht bestanden wird, wird die Datei in keiner Weise geändert.</span><span class="sxs-lookup"><span data-stu-id="850a6-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="850a6-172">Wenn eine URL zum Angeben einer Zeitstempel Stelle (Time Stamp Authority, TSA) übermittelt wird, wird diese Richtlinie auch auf den Zeitstempel angewendet.</span><span class="sxs-lookup"><span data-stu-id="850a6-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="850a6-173">*erhaltene*</span><span class="sxs-lookup"><span data-stu-id="850a6-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="850a6-174">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="850a6-174">Reserved.</span></span> <span data-ttu-id="850a6-175">Dieser Wert muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="850a6-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="850a6-176">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="850a6-176">Return value</span></span>

<span data-ttu-id="850a6-177">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="850a6-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="850a6-178">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="850a6-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="850a6-179">Mögliche Fehlercodes, die von dieser Funktion zurückgegeben werden, sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="850a6-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="850a6-180">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="850a6-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="850a6-181">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="850a6-181">Return code</span></span>                                                                                  | <span data-ttu-id="850a6-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="850a6-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="850a6-183"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="850a6-184">Wenn Sie den Parameter " *dwtimestampflags* " auf den Signatur Geber- **\_ Zeitstempel \_ Authenticode** festgelegt haben, können Sie den *dwFlags* -Parameter nicht auf **sig \_ Append** festlegen.</span><span class="sxs-lookup"><span data-stu-id="850a6-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="850a6-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="850a6-185">Requirements</span></span>



| <span data-ttu-id="850a6-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="850a6-186">Requirement</span></span> | <span data-ttu-id="850a6-187">Wert</span><span class="sxs-lookup"><span data-stu-id="850a6-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="850a6-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="850a6-188">Minimum supported client</span></span><br/> | <span data-ttu-id="850a6-189">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="850a6-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="850a6-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="850a6-190">Minimum supported server</span></span><br/> | <span data-ttu-id="850a6-191">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="850a6-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="850a6-192">DLL</span><span class="sxs-lookup"><span data-stu-id="850a6-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="850a6-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="850a6-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="850a6-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="850a6-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850a6-195">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="850a6-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="850a6-196">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="850a6-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="850a6-197">**Signerfresignercontext**</span><span class="sxs-lookup"><span data-stu-id="850a6-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
