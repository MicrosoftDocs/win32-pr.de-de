---
description: Zeitstempel des angegebenen Subjekts und gibt optional einen Zeiger auf eine Signatur Geber- \_ Kontext Struktur zurück, die einen Zeiger auf ein BLOB enthält. Diese Funktion kann verwendet werden, um die X. 509-Public Key-Infrastruktur, RFC 3161&\# 8211; kompatible Zeitstempel, auszuführen.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351455"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="83a3f-104">SignerTimeStampEx2-Funktion</span><span class="sxs-lookup"><span data-stu-id="83a3f-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="83a3f-105">Der **SignerTimeStampEx2** -Funktions Zeitstempel des angegebenen Subjekts und gibt optional einen Zeiger auf eine Signatur Geber- [**\_ Kontext**](signer-context.md) Struktur zurück, die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="83a3f-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="83a3f-106">Diese Funktion kann verwendet werden, um die X. 509-Public Key-Infrastruktur, RFC 3161 – kompatible, Zeitstempel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="83a3f-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="83a3f-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="83a3f-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="83a3f-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="83a3f-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="83a3f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="83a3f-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="83a3f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83a3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83a3f-111">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-112">-Wert, der den Typ des zu generierenden Zeitstempels angibt.</span><span class="sxs-lookup"><span data-stu-id="83a3f-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="83a3f-113">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="83a3f-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="83a3f-114">Die Werte schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="83a3f-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="83a3f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="83a3f-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="83a3f-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="83a3f-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="83a3f-117"><dt>**Signatur Geber- \_ Zeitstempel \_ Authenticode**</dt></span><span class="sxs-lookup"><span data-stu-id="83a3f-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="83a3f-118">Gibt einen Authenticode-Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="83a3f-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="83a3f-119"><dt>**Signatur Geber- \_ Zeitstempel \_ Timestampserver**</dt></span><span class="sxs-lookup"><span data-stu-id="83a3f-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="83a3f-120">Gibt einen RFC 3161 – kompatiblen Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="83a3f-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="83a3f-121">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-122">Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.</span><span class="sxs-lookup"><span data-stu-id="83a3f-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="83a3f-123">*pwszhttptimestamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-124">Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="83a3f-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="83a3f-125">*dwalgid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-126">Gibt einen Hash Algorithmus an, der zum Ausführen von RFC 3161 – kompatiblen Zeitstempeln verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83a3f-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="83a3f-127">Dieser Parameter wird bei Authenticode-Zeitstempeln ignoriert.</span><span class="sxs-lookup"><span data-stu-id="83a3f-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="83a3f-128">*psrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-129">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="83a3f-129">Optional.</span></span> <span data-ttu-id="83a3f-130">Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="83a3f-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="83a3f-131">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="83a3f-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="83a3f-132">*psipdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="83a3f-133">Optional.</span></span> <span data-ttu-id="83a3f-134">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen ( [*Subject Interface Package, subject Interface Package*](../secgloss/s-gly.md) ) weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="83a3f-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="83a3f-135">Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="83a3f-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="83a3f-136">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="83a3f-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="83a3f-137">*ppsignercontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83a3f-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="83a3f-138">Optional.</span></span> <span data-ttu-id="83a3f-139">Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="83a3f-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="83a3f-140">Wenn Sie die Signatur Geber- **\_ Kontext** Struktur nicht mehr verwenden, können Sie Sie durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="83a3f-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83a3f-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83a3f-141">Return value</span></span>

<span data-ttu-id="83a3f-142">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="83a3f-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="83a3f-143">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="83a3f-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="83a3f-144">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="83a3f-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83a3f-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83a3f-145">Requirements</span></span>



| <span data-ttu-id="83a3f-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83a3f-146">Requirement</span></span> | <span data-ttu-id="83a3f-147">Wert</span><span class="sxs-lookup"><span data-stu-id="83a3f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83a3f-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83a3f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="83a3f-149">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="83a3f-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83a3f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="83a3f-151">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83a3f-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="83a3f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="83a3f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83a3f-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83a3f-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83a3f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83a3f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a3f-155">**Signertimestamp**</span><span class="sxs-lookup"><span data-stu-id="83a3f-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="83a3f-156">**Signertimestampex**</span><span class="sxs-lookup"><span data-stu-id="83a3f-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 
