---
description: Zeitstempel des angegebenen Subjekts. Diese Funktion unterstützt das Zeitstempel von Authenticode. Verwenden Sie die SignerTimeStampEx2-Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Signertimestamp-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960453"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="a6a5f-105">Signertimestamp-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6a5f-105">SignerTimeStamp function</span></span>

<span data-ttu-id="a6a5f-106">Die **signertimestamp** -Funktion stempelt den angegebenen Betreff.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="a6a5f-107">Diese Funktion unterstützt das Zeitstempel von Authenticode.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="a6a5f-108">Verwenden Sie die [**SignerTimeStampEx2**](signertimestampex2.md) -Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="a6a5f-109">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="a6a5f-110">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a6a5f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6a5f-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="a6a5f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6a5f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a5f-113">*psubjetinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6a5f-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a5f-114">Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="a6a5f-115">*pwszhttptimestamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6a5f-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a5f-116">Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="a6a5f-117">*psrequest* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a6a5f-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a5f-118">Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="a6a5f-119">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="a6a5f-120">*psipdata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a6a5f-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a5f-121">Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="a6a5f-122">Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="a6a5f-123">Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a5f-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6a5f-124">Return value</span></span>

<span data-ttu-id="a6a5f-125">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="a6a5f-126">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="a6a5f-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="a6a5f-127">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="a6a5f-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a5f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6a5f-128">Requirements</span></span>



| <span data-ttu-id="a6a5f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6a5f-129">Requirement</span></span> | <span data-ttu-id="a6a5f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a6a5f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a5f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6a5f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a5f-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6a5f-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a6a5f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6a5f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a5f-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6a5f-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6a5f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a6a5f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6a5f-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6a5f-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
