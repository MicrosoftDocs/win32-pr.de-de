---
description: Zeitstempel des angegebenen Subjekts und unterstützen das Festlegen von Zeitstempeln für mehrere Signaturen.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128089"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="39e75-103">SignerTimeStampEx3-Funktion</span><span class="sxs-lookup"><span data-stu-id="39e75-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="39e75-104">Der **SignerTimeStampEx3** -Funktions Zeitstempel des angegebenen Subjekts und unterstützt das Festlegen von Zeitstempeln für mehrere Signaturen.</span><span class="sxs-lookup"><span data-stu-id="39e75-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="39e75-105">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="39e75-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="39e75-106">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="39e75-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="39e75-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39e75-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="39e75-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39e75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e75-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e75-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-110">Flag, das den Typ des zu generierenden Zeitstempels angibt.</span><span class="sxs-lookup"><span data-stu-id="39e75-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="39e75-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="39e75-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="39e75-112">Die Werte schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="39e75-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39e75-113">Wert</span><span class="sxs-lookup"><span data-stu-id="39e75-113">Value</span></span></th>
<th><span data-ttu-id="39e75-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="39e75-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="39e75-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="39e75-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="39e75-116">Gibt einen Authenticode-Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="39e75-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39e75-117">Authenticode ist nicht mehr der bevorzugte Typ des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="39e75-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="39e75-118">Die Unterstützung für Authenticode-Zeitstempel kann in Zukunft entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="39e75-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="39e75-119">Es wird empfohlen, stattdessen RFC 3161 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39e75-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="39e75-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="39e75-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="39e75-121">Gibt einen RFC 3161 – kompatiblen Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="39e75-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="39e75-122">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e75-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-123">Gibt die Sequenznummer der Signatur an, der der Zeitstempel hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="39e75-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="39e75-124">Wenn dieser Wert 0 (null) ist, wird die äußere Signatur mit einem Zeitstempel versehen.</span><span class="sxs-lookup"><span data-stu-id="39e75-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-125">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e75-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-126">Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39e75-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-127">*pwszhttptimestamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e75-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-128">Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="39e75-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-129">*pszalgorithmuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e75-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-130">Ein Hash Algorithmus, der zum Ausführen von RFC 3161 – kompatiblen Zeitstempeln verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39e75-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="39e75-131">Dieser Parameter wird bei Authenticode-Zeitstempeln ignoriert.</span><span class="sxs-lookup"><span data-stu-id="39e75-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-132">*psrequest* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="39e75-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="39e75-133">Optional.</span></span> <span data-ttu-id="39e75-134">Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="39e75-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="39e75-135">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="39e75-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-136">*psipdata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="39e75-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-137">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="39e75-137">Optional.</span></span> <span data-ttu-id="39e75-138">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen ( [*Subject Interface Package, subject Interface Package*](../secgloss/s-gly.md) ) weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="39e75-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="39e75-139">Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="39e75-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="39e75-140">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="39e75-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-141">*ppsignercontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39e75-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-142">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="39e75-142">Optional.</span></span> <span data-ttu-id="39e75-143">Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="39e75-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="39e75-144">Wenn Sie die Signatur Geber- **\_ Kontext** Struktur nicht mehr verwenden, können Sie Sie durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="39e75-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-145">*pcryptopolicy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="39e75-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e75-146">Falls vorhanden, ein Zeiger auf eine [**CERT \_ Strong \_ Sign \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) Structure-Struktur, die die Parameter enthält, die für die Überprüfung auf starke Signaturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39e75-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="39e75-147">Der Zeitstempel muss diese Kryptografierichtlinie bestehen.</span><span class="sxs-lookup"><span data-stu-id="39e75-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="39e75-148">*erhaltene*</span><span class="sxs-lookup"><span data-stu-id="39e75-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="39e75-149">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="39e75-149">Reserved.</span></span> <span data-ttu-id="39e75-150">Dieser Wert muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="39e75-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e75-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39e75-151">Return value</span></span>

<span data-ttu-id="39e75-152">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="39e75-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="39e75-153">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="39e75-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="39e75-154">Mögliche Fehlercodes, die von dieser Funktion zurückgegeben werden, sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="39e75-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="39e75-155">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="39e75-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39e75-156">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="39e75-156">Return code</span></span></th>
<th><span data-ttu-id="39e75-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39e75-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="39e75-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="39e75-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="39e75-159">Dieser Fehler kann unter folgenden Bedingungen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="39e75-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="39e75-160">Sie müssen entweder <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> oder <strong>SIGNER_TIMESTAMP_RFC3161</strong> für den <em>dwFlags</em> -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="39e75-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="39e75-161">Der <em></em> beibehaltene Parameter muss <strong>null</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="39e75-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="39e75-162">Wenn Sie das <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> -Flag im <em>dwFlags</em> -Parameter festgelegt haben, müssen Sie den <em>dwIndex</em> -Parameter auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="39e75-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="39e75-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39e75-163">Requirements</span></span>



| <span data-ttu-id="39e75-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39e75-164">Requirement</span></span> | <span data-ttu-id="39e75-165">Wert</span><span class="sxs-lookup"><span data-stu-id="39e75-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e75-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39e75-166">Minimum supported client</span></span><br/> | <span data-ttu-id="39e75-167">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39e75-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="39e75-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39e75-168">Minimum supported server</span></span><br/> | <span data-ttu-id="39e75-169">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39e75-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="39e75-170">DLL</span><span class="sxs-lookup"><span data-stu-id="39e75-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39e75-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e75-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e75-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39e75-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e75-173">**Signertimestamp**</span><span class="sxs-lookup"><span data-stu-id="39e75-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="39e75-174">**Signertimestampex**</span><span class="sxs-lookup"><span data-stu-id="39e75-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="39e75-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="39e75-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 
