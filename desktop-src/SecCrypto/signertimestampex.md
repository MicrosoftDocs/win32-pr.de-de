---
description: Zeitstempel des angegebenen Subjekts und gibt optional einen Zeiger auf eine Signatur Geber- \_ Kontext Struktur zurück, die einen Zeiger auf ein BLOB enthält.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: Signertimestampex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758772"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="72129-103">Signertimestampex-Funktion</span><span class="sxs-lookup"><span data-stu-id="72129-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="72129-104">Die **signertimestampex** -Funktion stempelt das angegebene Subjekt und gibt optional einen Zeiger auf eine Signatur Geber- [**\_ Kontext**](signer-context.md) Struktur zurück, die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="72129-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="72129-105">Diese Funktion unterstützt das Zeitstempel von Authenticode.</span><span class="sxs-lookup"><span data-stu-id="72129-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="72129-106">Verwenden Sie die [**SignerTimeStampEx2**](signertimestampex2.md) -Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="72129-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="72129-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="72129-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="72129-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="72129-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="72129-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="72129-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="72129-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72129-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72129-111">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72129-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72129-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="72129-112">Reserved.</span></span> <span data-ttu-id="72129-113">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="72129-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="72129-114">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72129-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72129-115">Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.</span><span class="sxs-lookup"><span data-stu-id="72129-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="72129-116">*pwszhttptimestamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72129-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72129-117">Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="72129-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="72129-118">*psrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72129-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72129-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="72129-119">Optional.</span></span> <span data-ttu-id="72129-120">Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="72129-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="72129-121">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="72129-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="72129-122">*psipdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72129-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72129-123">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="72129-123">Optional.</span></span> <span data-ttu-id="72129-124">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen ( [*Subject Interface Package, subject Interface Package*](../secgloss/s-gly.md) ) weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="72129-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="72129-125">Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="72129-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="72129-126">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="72129-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="72129-127">*ppsignercontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72129-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72129-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="72129-128">Optional.</span></span> <span data-ttu-id="72129-129">Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="72129-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="72129-130">Wenn Sie die Signatur Geber- **\_ Kontext** Struktur nicht mehr verwenden, können Sie Sie durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="72129-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72129-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72129-131">Return value</span></span>

<span data-ttu-id="72129-132">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="72129-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="72129-133">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="72129-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="72129-134">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="72129-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72129-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72129-135">Requirements</span></span>



| <span data-ttu-id="72129-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72129-136">Requirement</span></span> | <span data-ttu-id="72129-137">Wert</span><span class="sxs-lookup"><span data-stu-id="72129-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72129-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72129-138">Minimum supported client</span></span><br/> | <span data-ttu-id="72129-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72129-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72129-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72129-140">Minimum supported server</span></span><br/> | <span data-ttu-id="72129-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72129-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72129-142">DLL</span><span class="sxs-lookup"><span data-stu-id="72129-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72129-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72129-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72129-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72129-144">See also</span></span>

<dl> <span data-ttu-id="72129-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="72129-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="72129-146">**Signertimestamp**</span><span class="sxs-lookup"><span data-stu-id="72129-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 
